# challenge



class Point:

    def __init__(self, x, y):
    
        self.x = x
        self.y = y


def onSegment(p, q, r):

    if ((q.x <= max(p.x, r.x)) and (q.x >= min(p.x, r.x)) and
            (q.y <= max(p.y, r.y)) and (q.y >= min(p.y, r.y))):
        return True
    return False


def orientation(p, q, r):


    val = (float(q.y - p.y) * (r.x - q.x)) - (float(q.x - p.x) * (r.y - q.y))
    if (val > 0):


        return 1
    elif (val < 0):


        return 2
    else:


        return 0



def doIntersect(p1, q1, p2, q2):

    o1 = orientation(p1, q1, p2)
    o2 = orientation(p1, q1, q2)
    o3 = orientation(p2, q2, p1)
    o4 = orientation(p2, q2, q1)


    if ((o1 != o2) and (o3 != o4)):
        return True




    if ((o1 == 0) and onSegment(p1, p2, q1)):
        return True


    if ((o2 == 0) and onSegment(p1, q2, q1)):
        return True


    if ((o3 == 0) and onSegment(p2, p1, q2)):
        return True

    if ((o4 == 0) and onSegment(p2, q1, q2)):
        return True


    return False



p1 = Point(1, 0)
q1 = Point(8, 3)
p2 = Point(8, 8)
q2 = Point(1, 5)
p=(3,5)
n=()
polygon=()
def isInside( polygon, n,Point p):

    if n<3:
        return False
             extreme=(INF,p.y)

    count=0
    i=0
        next=(i+1)%n

        if doIntersect(polygon[i],p,polygon[next])==0:
            if (orientation(polygon[i],p,polygon[next]))==0:

                return onSegment(polygon[i],p,polygon[next]):
            count=+
        i=next
    whilei!=0:
        count and 1


else:
    print(False)

p1 = Point(-3, 2)
q1 = Point(-2, -0.8)
p2 = Point(0, 1.2)
q2 = Point(2.2, 0)
q3=point(2,4.5)
p=(0,0)
n=[]
polygon=[]
def isInside( polygon[], n,Point p):

    if(n<3):
        return False
             extreme={INF,p.y}

    count=0
    i=0
        next=(i+1)%n

        if doIntersect(polygon[i],p,polygon[next])==0:
            if (orientation(polygon[i],p,polygon[next])==0):

                return onSegment(polygon[i],p,polygon[next]):
            count+=
        i=next
    while(i!=0):
        count


else:
    print(False)

