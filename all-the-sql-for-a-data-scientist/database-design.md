# Database Design

![Database Design for Instagram](<../.gitbook/assets/image (27).png>)

```
CREATE TABLE "public.Users" (
	"password" varchar(255) NOT NULL,
	"profile_pic" varchar(255) NOT NULL,
	"id" serial(11) NOT NULL,
	"email_id" varchar(255) NOT NULL,
	"fullname" varchar(255) NOT NULL,
	CONSTRAINT "Users_pk" PRIMARY KEY ("id")
) WITH (
  OIDS=FALSE
);



CREATE TABLE "public.Posts" (
	"video_url" varchar(255) NOT NULL,
	"id" integer(255) NOT NULL,
	"user_id" integer(11) NOT NULL,
	CONSTRAINT "Posts_pk" PRIMARY KEY ("id")
) WITH (
  OIDS=FALSE
);



CREATE TABLE "public.likes" (
	"id" integer(11) NOT NULL,
	"user_id" integer(11) NOT NULL,
	"post_id" integer(11) NOT NULL,
	CONSTRAINT "likes_pk" PRIMARY KEY ("id")
) WITH (
  OIDS=FALSE
);



CREATE TABLE "public.comment" (
	"id" integer(11) NOT NULL,
	"text" TEXT NOT NULL,
	"user_id" integer(11) NOT NULL,
	"post_id" integer(11) NOT NULL,
	CONSTRAINT "comment_pk" PRIMARY KEY ("id")
) WITH (
  OIDS=FALSE
);



CREATE TABLE "public.friend requests" (
	"sender_id" integer(11) NOT NULL,
	"receiver_id" integer(11) NOT NULL,
	"status" BOOLEAN NOT NULL,
	"id" integer(11) NOT NULL,
	CONSTRAINT "friend requests_pk" PRIMARY KEY ("id")
) WITH (
  OIDS=FALSE
);




ALTER TABLE "Posts" ADD CONSTRAINT "Posts_fk0" FOREIGN KEY ("user_id") REFERENCES "Users"("id");

ALTER TABLE "likes" ADD CONSTRAINT "likes_fk0" FOREIGN KEY ("user_id") REFERENCES "Users"("id");
ALTER TABLE "likes" ADD CONSTRAINT "likes_fk1" FOREIGN KEY ("post_id") REFERENCES "Posts"("id");

ALTER TABLE "comment" ADD CONSTRAINT "comment_fk0" FOREIGN KEY ("user_id") REFERENCES "Users"("id");
ALTER TABLE "comment" ADD CONSTRAINT "comment_fk1" FOREIGN KEY ("post_id") REFERENCES "Posts"("id");

ALTER TABLE "friend requests" ADD CONSTRAINT "friend requests_fk0" FOREIGN KEY ("sender_id") REFERENCES "Users"("id");
ALTER TABLE "friend requests" ADD CONSTRAINT "friend requests_fk1" FOREIGN KEY ("receiver_id") REFERENCES "Users"("id");

```
