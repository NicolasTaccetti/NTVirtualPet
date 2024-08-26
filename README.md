// Nicolas Taccetti
// 8/23/24
// Create a virtual pet with shape functions. Learn a workflow between a code IDE and GitHub to document and share computer programs. 

public void setup() {
    size(400, 400);
  }
public void draw() {
    background(0);
    pushMatrix();//beak
    translate(77, 16);
    rotate(radians(10));
    stroke(209, 23, 48);
    strokeWeight(3);
    fill(0);
    ellipse(0, 0, 50, 8);
    popMatrix();//covering ellipse
    noStroke();
    pushMatrix();
    translate(77, 18);
    rotate(radians(10));
    fill(0);
    ellipse(0, 0, 50, 8);
    popMatrix();
    
    noStroke();
    fill(0, 13, 69); ellipse(106, 40, 50, 50); //head
    fill(18, 21, 217); ellipse(103, 38, 45, 45); smooth(); triangle(105, 16, 81, 33, 84, 16);
    fill(2, 82, 57);//feathers
    arc(97, 49, 7, 7, radians(45), radians(225));
    arc(106, 50, 10, 10, radians(45), radians(225));
    arc(107, 38, 7, 7, radians(45), radians(225));
    arc(118, 38, 7, 7, radians(45), radians(225));
    
    smooth();//eye
    fill(2, 82, 57);
    noStroke();
    ellipse(97, 24, 15, 10);
    pushMatrix();
    translate(97, 24);
    rotate(radians(45));
    fill(2, 82, 57);
    ellipse(0, 0, 15, 10);
    popMatrix();
    fill(0);
    ellipse(95, 21, 7, 7);
    stroke(255);
    point(96, 19);
    
    //body
    noStroke();
    fill(18, 21, 217);
    triangle(128, 65, 198, 145, 215, 136);
    triangle(165, 133, 150, 131, 128, 65);
    triangle(131, 115, 128, 65, 120, 111);
    fill(2, 82, 57);
    triangle(128, 65, 215, 136, 217, 122);
    triangle(128, 65, 174, 126, 165, 133);
    triangle(142, 111, 128, 65, 131, 115);
    triangle(191, 103, 191, 98, 128, 65);
    fill(0, 13, 69);
    triangle(191, 150, 128, 65, 198, 145);
    triangle(146, 131, 128, 65, 150, 131);
    
    // fill(209, 23, 48);//old(moveable)wings
    // triangle(121, 68, 107, 99, 57, 91);
    // triangle(132, 62, 149, 45, 169, 65);
    // triangle(149, 45, 169, 65, 190, 62);
    // fill(176, 2, 10);
    // triangle(107, 99, 57, 91, 47, 128);

    //wing1, left (arcs in ascending order)
    fill(117, 0, 0);
    stroke(117, 0, 0);
    arc(108, 70, 30, 30, 0, radians(35));
    arc(108, 70, 30, 40, radians(25), radians(70));
    fill(150, 2, 2);
    arc(108, 70, 60, 34, radians(67), radians(90));
    fill(176, 2, 10);
    arc(108, 70, 195, 42, radians(88), radians(110));
    arc(108, 70, 150, 54, radians(99), radians(120));
    fill(199, 14, 14);
    arc(108, 70, 130, 80, radians(122), radians(148));
    fill(235, 19, 26);
    arc(108, 70, 130, 90, radians(150), radians(170));
    arc(108, 70, 130, 100, radians(170), radians(190));
    fill(199, 14, 14);
    arc(108, 70, 137, 82, radians(190), radians(210));
    //wing2, right (arcs in descending order)
    arc(137, 54, 92, 70, radians(295), radians(308));
    fill(235, 19, 26);
    arc(137, 54, 92, 64, radians(305), radians(328));
    arc(137, 54, 86, 67, radians(330), radians(353));
    arc(137, 54, 86, 53, radians(-10), radians(10));
    fill(176, 2, 10);
    arc(137, 54, 80, 18, radians(23), radians(45));
    arc(137, 54, 60, 24, radians(29), radians(65));
    fill(117, 0, 0);
    arc(137, 54, 38, 22, radians(56), radians(82));
    arc(137, 54, 20, 20, radians(77), radians(115));

    noStroke();//moon
    fill(92, 88, 53);
    ellipse(332, 45, 65, 65);
    fill(245, 233, 105);
    ellipse(332, 45, 50, 50);
    fill(184, 165, 2);
    ellipse(342, 28, 8, 8);
    ellipse(346, 36, 4, 4);
    ellipse(322, 44, 13, 13);
    ellipse(337, 59, 10, 10);

    
    stroke(89, 58, 59);//feet
    strokeWeight(3);
    line(206, 145, 228, 157);
    line(185, 144, 186, 156);
    stroke(130, 100, 101);
    fill(0);
    strokeWeight(2);
    arc(224, 154, 10, 10, radians(45), radians(225));
    arc(226, 150, 10, 10, radians(0), radians(180));
    arc(217, 147, 6, 6, radians(45), radians(225));
    arc(190, 156, 5, 14, radians(10), radians(190));
    arc(182, 156, 5, 14, radians(350), radians(530));
    arc(184, 151, 3, 6, radians(45), radians(225));
    line(186, 166, 186, 154);

    //other bird
    noStroke();
    fill(209, 23, 48);
    ellipse(273, 85, 7, 5);
    fill(18, 21, 217);
    ellipse(267, 77, 7, 7);
    ellipse(268, 88, 10, 20);
    fill(209, 23, 48);
    ellipse(263, 85, 7, 3);
    fill(2, 82, 57);
    triangle(271, 84, 279, 97, 270, 100);

    //coordinates
    fill(255);
    text("("+mouseX+","+mouseY+")", mouseX,mouseY);
  }
  //side note: for some reason, I can't do a star slash function, so I'm just using double slash for text
