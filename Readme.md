### EasyConomy / EasySkills / SkillChange

or another random name

EasyConomy is a place to exchange skills and services for other skills and services and BTC

----------------------

Skills
model:

User
  btc_address

UserSkill
  user
  skill
  [need/have]

Skill
  experience
  price (price per hour)
  links
  #feedbacks


------

Flow:

@user1 = { name: "Ali" }
  POST /users/makevoid/skills/programming/request
    request = {
      skill: "programming"
      hours: 1..3
      price: 30_mbtc # per hour
    }


@user2 = { name: "Bob" }
  GET /requests
    requests = [<New Request>]

-> ACCEPT / DENY / MODIFY ?

---

ACCEPT

goes to the Assignments phase

---

DENY

cancels the request

---

MODIFY

modify hours and price: requests acceptance from the other user


---------

Assignment phase

Total Amount: <amount>

Delivery in: <delivery_time>

Assignment: Initial code review

Assignment text:
Please review this code and tell me if it's worth proceeding this way and estimate how much hours of refactoring are needed

-----

Done:
  - Initial code review

Worked: (3 hours)<time>

Amount Sent: (240 mbtc) <amount>


-----

New Assignment:


etc


----






anyway it's just an idea thrown there


-----

models tree:

- user

- skills
  - need
  - have

---

User
  Experience experience_level 0..5 (and none) ExperienceLeve.new("none")

Skill
  Price


---

examples:

GET /skills/programming
GET /skills

---

POST /skills/programming
  { name: "", experience: <Experience>, links: [], price: <Price> } # , feedbacks: []

---

GET /users/makevoid/skills
  %skill programming

----

GET /skills

---


POST /skills
  - name
  - price (#price per hour)
  - area

---


