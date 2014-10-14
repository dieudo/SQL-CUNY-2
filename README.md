607week7assignement
===================
-- Table: "INSTRUCTORS"

-- DROP TABLE "INSTRUCTORS";

CREATE TABLE "INSTRUCTORS"
(
  "ID" integer NOT NULL,
  "Name" character varying NOT NULL,
  "NumberOfYears" numeric NOT NULL,
  "DOB" date NOT NULL,
  CONSTRAINT "ID" PRIMARY KEY ("ID")
)
WITH (
  OIDS=FALSE
);
ALTER TABLE "INSTRUCTORS"
  OWNER TO postgres;
  
  INSERT INTO "INSTRUCTORS"(
            "ID", "Name", "NumberOfYears", "DOB")
    VALUES ('1','Paul','5', '1960-01-01'),('2','Andy','4','1970-01-01'),('3','Mike','4','1975-01-01');
    
    
    -- Table: "STUDENTS"

-- DROP TABLE "STUDENTS";

CREATE TABLE "STUDENTS"
(
  "STUDENT-ID" integer NOT NULL,
  "CITY" character(1) NOT NULL,
  "ID" integer NOT NULL,
  "StudentName" character varying,
  CONSTRAINT "STUDENTS_pkey" PRIMARY KEY ("STUDENT-ID"),
  CONSTRAINT "STUDENTS_ID_fkey" FOREIGN KEY ("ID")
      REFERENCES "INSTRUCTORS" ("ID") MATCH SIMPLE
      ON UPDATE NO ACTION ON DELETE NO ACTION
)
WITH (
  OIDS=FALSE
);
ALTER TABLE "STUDENTS"
  OWNER TO postgres;
  
INSERT INTO "STUDENTS"(
            "STUDENT-ID", "CITY", "ID", "StudentName")
    VALUES ('10','Y', '1','Dieudonne'),('11','A','2','Jare'),('12','J','1','NULL');
    
    
    
    SELECT
    StudentName,
    FROM STUDENTS
    JOIN INSTRUCTORS 
    ON STUDENTS.ID=INSTRUCTORS.ID
    WHERE STUDENTS.StudentName IS NULL
    
    result:('12','J','1','NULL')
    
    SELECT 
    CITY,
    FROM STUDENTS
    LEFT JOIN INSTRUCTORS
    ON STUDENTS.ID=INSTRUCTORS.ID

    
    

  
  
