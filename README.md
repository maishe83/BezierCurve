BezierCurve
===========

Generates a Bezier Curve in euclidean or quaternion space with differentiable acceleration.

Vector Version

std::vector<Vector3f> waypoints; /* Length N */
std::vector<float> timeForEachSegment; /* Length N - 1 */

curve = new BezierCurve(waypoints, timeForEachSegment);

p = curve->positionAtTime(t);
v = curve->velocityAtTime(t);
a = curve->accelerationAtTime(t);

Quaternion Version

std::vector<Quaternionf> waypoints; /* Length N */
std::vector<float> timeForEachSegment; / Length N - 1 */

curve = new BezierCurve(waypoints,timeForEachSegment);

q = curve->quaternionAtTime(t);
w = curve->angularVelocityAtTime(t); /* Vector3f */

Requirements: Eigen3
