<template>
  <div id="app" @contextmenu.prevent="openMenu($event)">
    <ul
      v-show="visible"
      :style="{ left: left + 'px', top: top + 'px' }"
      class="contextmenu"
    >
      <li @click="goToGithub">这就去Github给作者点赞!</li>
    </ul>
    <div id="github"></div>
    <a href="https://github.com/1076269190"
      ><svg
        t="1658497606268"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="2260"
        id="svgA"
      >
        <path
          d="M1023.560892 524.587752c0 114.331752-32.549236 217.148443-97.647709 308.450075-65.047295 91.301632-149.132822 154.455339-252.205404 189.512299-11.975662 2.303012-20.778286 0.716493-26.305515-4.759558a27.584966 27.584966 0 0 1-8.342021-20.471218V853.150798c0-44.166653-11.566238-76.511177-34.647536-96.982394a446.272549 446.272549 0 0 0 68.32269-12.282731c20.16415-5.476051 41.044792-14.329852 62.590748-26.612583a187.311643 187.311643 0 0 0 53.992837-45.446104c14.432209-18.014672 26.203159-41.914819 35.312851-71.751618 9.109692-29.8368 13.664538-64.074912 13.664538-102.765514 0-55.118754-17.554069-102.049021-52.61103-140.739623 16.376974-41.454216 14.636921-87.872703-5.373695-139.357815-12.436265-4.094244-30.399759-1.535341-53.941659 7.523172a355.17563 355.17563 0 0 0-61.311297 30.041513l-25.333132 16.376974a462.137743 462.137743 0 0 0-127.945112-17.707604 462.137743 462.137743 0 0 0-127.945111 17.758782 589.571074 589.571074 0 0 0-28.301459-18.424096c-11.77095-7.31846-30.34858-16.069906-55.681713-26.305515-25.281954-10.235609-44.422543-13.306292-57.31941-9.212048-19.498835 51.433935-21.085354 97.852421-4.606024 139.306637-35.108139 38.690602-52.713386 85.620869-52.713386 140.739623 0 38.690602 4.606024 72.826357 13.715716 102.458445 9.109692 29.58091 20.778286 53.481057 34.954605 71.700441a180.658498 180.658498 0 0 0 53.634591 45.753172c21.545957 12.282731 42.477777 21.18771 62.641926 26.612583 20.215328 5.527229 42.989557 9.621472 68.32269 12.333909-17.758781 16.376974-28.659705 39.867697-32.651593 70.369811a129.941055 129.941055 0 0 1-29.990334 10.235609 184.087426 184.087426 0 0 1-37.974109 3.428929c-14.688099 0-29.171485-4.913092-43.654872-14.688099-14.432209-9.826185-26.766117-24.053681-37.001726-42.682489a109.162769 109.162769 0 0 0-32.293346-35.517563c-13.101579-9.109692-24.104859-14.585743-33.009839-16.376974l-13.306292-2.047122c-9.314404 0-15.762838 1.023561-19.345301 3.070683-3.582463 2.047122-4.606024 4.606024-3.326572 7.83024a37.769397 37.769397 0 0 0 5.987831 9.570295 49.182101 49.182101 0 0 0 8.700267 8.188487l4.606024 3.377751c9.826185 4.606024 19.447657 13.255114 29.017952 25.998447 9.570294 12.743333 16.581686 24.360749 20.982998 34.80107l6.653146 15.71166c5.783119 17.298179 15.558126 31.320963 29.376197 42.017174 13.766894 10.747389 28.659705 17.554069 44.627255 20.471218 15.96755 2.968327 31.423319 4.606024 46.316131 4.810736 14.841633 0.204712 27.22672-0.562958 37.001726-2.405368l15.302235-2.712436c0 17.298179 0.102356 37.564685 0.358247 60.799517l0.307068 36.848192c0 8.188487-2.86597 15.046345-8.700268 20.471218-5.731941 5.527229-14.636921 7.113748-26.612583 4.810736-103.072582-35.056961-187.158109-98.261846-252.205404-189.512299C32.549236 741.736195 0 638.919504 0 524.587752c0-95.191163 22.876586-182.910331 68.629758-263.31104a516.028224 516.028224 0 0 1 186.288082-190.894106A491.309228 491.309228 0 0 1 511.780446 0.012795a491.309228 491.309228 0 0 1 256.913784 70.369811 516.028224 516.028224 0 0 1 186.236905 190.894106C1000.684306 341.626242 1023.560892 429.447767 1023.560892 524.587752z"
          fill="#ffffff"
          p-id="2261"
        ></path></svg
    ></a>
    <a href="">
      <svg
        t="1658498528685"
        class="icon"
        viewBox="0 0 1024 1024"
        version="1.1"
        xmlns="http://www.w3.org/2000/svg"
        p-id="2468"
        id="refresh"
      >
        <path
          d="M834.2 531.9c0 187.7-152.2 339.9-339.9 339.9S154.4 719.7 154.4 531.9c0-187.7 152.2-339.9 339.9-339.9 124.8 0 233.6 67.5 292.7 167.7h63.8c-64.1-132.5-199.4-224.1-356.5-224.1C275.4 135.6 98 313.1 98 531.9s177.4 396.3 396.3 396.3 396.3-177.4 396.3-396.3c0-4.9-0.6-9.7-0.7-14.6 0 0-1.4-28.9-28.7-28.9-30.6 0-27.6 28.9-27.6 28.9 0.1 4.9 0.6 9.7 0.6 14.6z"
          fill="#2c2c2c"
          p-id="2469"
        ></path>
        <path
          d="M853.9 101.1C843 100 833.1 108 832 119l-21.6 213.7c-1.1 10.9-11 19-21.9 17.9L574.8 329c-10.9-1.1-20.8 6.9-21.9 17.9l-1.5 14.8c-1.1 10.9 6.9 20.8 17.9 21.9L783 405.2c10.9 1.1 19.9 2 19.9 2s9 0.9 19.9 2l14.8 1.5c10.9 1.1 20.8-6.9 21.9-17.9l27.1-268.3c1.1-10.9-6.9-20.8-17.9-21.9l-14.8-1.5z"
          fill="#2c2c2c"
          p-id="2470"
        ></path></svg
    ></a>
    <div id="cover" v-show="ifCome">
      <h1 class="animate__animated animate__fadeIn">Animate3DModel</h1>
      <h3
        class="animate__animated animate__fadeIn animate__delay-2s"
        @click="comeIn"
      >
        开始体验
      </h3>
    </div>
    <div v-show="ifStart" id="two">
      <h2>"选择上传本地模型或者选用预存模型"</h2>
      <div id="option">
        <input type="file" class="file" id="file" @change="setup($event)" />
        <div class="left">
          <el-select
            v-model="character"
            placeholder="请选择"
            :Popper-append-to-body="false"
          >
            <el-option
              v-for="item in options"
              :key="item.value"
              :label="item.label"
              :value="item.value"
            >
            </el-option>
          </el-select>
          <h1 @click="start()" class="start-btn">选好了！</h1>
        </div>
      </div>
    </div>
    <div v-show="ifShow">
      <div id="recode">
        <div id="endBtn">
          <svg
            t="1658494274244"
            class="icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="3147"
          >
            <path
              d="M512 938.666667C276.352 938.666667 85.333333 747.648 85.333333 512S276.352 85.333333 512 85.333333s426.666667 191.018667 426.666667 426.666667-191.018667 426.666667-426.666667 426.666667zM384 384v256h256V384H384z"
              p-id="3148"
              fill="#ffffff"
            ></path></svg
          >结束录制
        </div>
        <div id="startBtn">
          <svg
            t="1658493963021"
            class="icon"
            viewBox="0 0 1024 1024"
            version="1.1"
            xmlns="http://www.w3.org/2000/svg"
            p-id="2770"
          >
            <path
              d="M512 938.666667C276.352 938.666667 85.333333 747.648 85.333333 512S276.352 85.333333 512 85.333333s426.666667 191.018667 426.666667 426.666667-191.018667 426.666667-426.666667 426.666667zM453.205333 359.04a17.066667 17.066667 0 0 0-26.538666 14.165333v277.589334a17.066667 17.066667 0 0 0 26.538666 14.165333l208.170667-138.752a17.066667 17.066667 0 0 0 0-28.416l-208.213333-138.752z"
              p-id="2771"
              fill="#ffffff"
            ></path></svg
          >开始录制
        </div>
      </div>
      <div class="preview" id="preview">
        <video class="input_video" width="1280px" height="720px"></video>
        <canvas class="guides"></canvas>
      </div>
    </div>
  </div>
</template>

<script>
import "animate.css";
import * as Kalidokit from "kalidokit";
export default {
  name: "App",
  data() {
    return {
      ifCome: true,
      ifStart: false,
      ifShow: false,
      options: [
        {
          value: "/static/vrm/3775384893171830519.vrm",
          label: "黄毛",
        },
        {
          value: "/static/vrm/0zm0h120009p2fmwcDBAE-044-135e73c7f840_Ashtra(4).vrm",
          label: "白毛",
        },
      ],
      character: "",
      ifRecoding: false,
      recodeData: [],
      visible: false,
      top: 0,
      left: 0,
    };
  },
  methods: {
    //start
    openMenu(e) {
      var x = e.pageX;
      var y = e.pageY;
      this.top = y;
      this.left = x;
      this.visible = true; //在这里控制右键菜单的打开
    },
    //close
    closeMenu() {
      this.visible = false;
    },
    goToGithub(){
      window.location.href = 'https://github.com/1076269190';
    },
    start() {
      console.log(this.character)
      if (this.character === "") return;
      this.ifStart = false;
      this.ifShow = true;

      let character = this.$data.character

      //Import Helper Functions from Kalidokit
      const remap = Kalidokit.Utils.remap;
      const clamp = Kalidokit.Utils.clamp;
      const lerp = Kalidokit.Vector.lerp;

      /////////////////////////
      /* THREEJS WORLD SETUP */
      /////////////////////////

      let currentVrm;

      // renderer
      const renderer = new THREE.WebGLRenderer({ alpha: true }); //创建渲染器对象
      renderer.setSize(window.innerWidth * 0.95, window.innerHeight * 0.95); //设置renderer高宽
      renderer.setPixelRatio(window.devicePixelRatio); //设置renderer像素比
      document.body.appendChild(renderer.domElement);

      // camera
      const orbitCamera = new THREE.PerspectiveCamera(
        35,
        window.innerWidth / window.innerHeight,
        0.1,
        1000
      ); //设置透视照相机
      orbitCamera.position.set(0.0, 1.4, 5); //设置照相机的水平，竖直，远近的球形比

      // camera controls
      const orbitControls = new THREE.OrbitControls(
        orbitCamera,
        renderer.domElement
      );
      orbitControls.screenSpacePanning = true; //定义当平移的时候摄像机的位置将如何移动。如果为true，摄像机将在屏幕空间内平移。否则，摄像机将在与摄像机向上方向垂直的平面中平移。
      orbitControls.target.set(0.0, 1.4, 0); //控制器的焦点
      orbitControls.update(); //更新控制器。必须在摄像机的变换发生任何手动改变后调用

      // scene
      const scene = new THREE.Scene();

      // light
      const light = new THREE.DirectionalLight(0xffffff); //灯光（颜色）
      light.position.set(1.0, 1.0, 1.0).normalize(); //设置灯光位置
      scene.add(light);

      // Main Render Loop
      const clock = new THREE.Clock(); //时钟 封装于Date()

      function animate() {
        requestAnimationFrame(animate);

        if (currentVrm) {
          // Update model to render physics
          currentVrm.update(clock.getDelta());
        }
        renderer.render(scene, orbitCamera);
      }
      animate();

      /////////////////////////
      /* VRM CHARACTER SETUP */
      /////////////////////////

      // Import Character VRM
      const loader = new THREE.GLTFLoader(); //GLTF加载器
      loader.crossOrigin = "anonymous";
      // Import model from URL, add your own model here
      loader.load(
        character,
        (gltf) => {
          THREE.VRMUtils.removeUnnecessaryJoints(gltf.scene);

          THREE.VRM.from(gltf).then((vrm) => {
            scene.add(vrm.scene);
            currentVrm = vrm;
            currentVrm.scene.rotation.y = Math.PI; // Rotate model 180deg to face camera
          });
        },

        (progress) =>
          console.log(
            "Loading model...",
            100.0 * (progress.loaded / progress.total),
            "%"
          ),

        (error) => console.error(error)
      );

      //////////////////////////////
      /* BoneNode change function */
      //////////////////////////////

      // Animate Rotation Helper function
      const rigRotation = (
        name,
        rotation = { x: 0, y: 0, z: 0 },
        dampener = 1,
        lerpAmount = 0.3
      ) => {
        if (!currentVrm) {
          return;
        }
        const Part = currentVrm.humanoid.getBoneNode(
          THREE.VRMSchema.HumanoidBoneName[name]
        );
        if (!Part) {
          return;
        }

        let euler = new THREE.Euler( //创建欧拉对象
          rotation.x * dampener,
          rotation.y * dampener,
          rotation.z * dampener,
          rotation.rotationOrder || "XYZ"
        );
        let quaternion = new THREE.Quaternion().setFromEuler(euler); //四元数
        Part.quaternion.slerp(quaternion, lerpAmount); // interpolate
      };

      // Animate Position Helper Function
      const rigPosition = (
        name,
        position = { x: 0, y: 0, z: 0 },
        dampener = 1,
        lerpAmount = 0.3
      ) => {
        if (!currentVrm) {
          return;
        }
        const Part = currentVrm.humanoid.getBoneNode(
          THREE.VRMSchema.HumanoidBoneName[name]
        );
        if (!Part) {
          return;
        }
        let vector = new THREE.Vector3(
          position.x * dampener,
          position.y * dampener,
          position.z * dampener
        );
        Part.position.lerp(vector, lerpAmount); // interpolate
      };

      let oldLookTarget = new THREE.Euler();
      const rigFace = (riggedFace) => {
        if (!currentVrm) {
          return;
        }
        rigRotation("Neck", riggedFace.head, 0.7);

        // 混合形状和预设名称模式
        const Blendshape = currentVrm.blendShapeProxy;
        const PresetName = THREE.VRMSchema.BlendShapePresetName;

        // 没有眨眼的简单例子。基于旧混合形状插值，然后使用“Kalidokit”辅助函数稳定闪烁。
        // for VRM, 1 is closed, 0 is open.
        riggedFace.eye.l = lerp(
          clamp(1 - riggedFace.eye.l, 0, 1),
          Blendshape.getValue(PresetName.Blink),
          0.5
        );
        riggedFace.eye.r = lerp(
          clamp(1 - riggedFace.eye.r, 0, 1),
          Blendshape.getValue(PresetName.Blink),
          0.5
        );
        riggedFace.eye = Kalidokit.Face.stabilizeBlink(
          riggedFace.eye,
          riggedFace.head.y
        );
        Blendshape.setValue(PresetName.Blink, riggedFace.eye.l);

        // 插值并设置嘴混合形状
        Blendshape.setValue(
          PresetName.I,
          lerp(riggedFace.mouth.shape.I, Blendshape.getValue(PresetName.I), 0.5)
        );
        Blendshape.setValue(
          PresetName.A,
          lerp(riggedFace.mouth.shape.A, Blendshape.getValue(PresetName.A), 0.5)
        );
        Blendshape.setValue(
          PresetName.E,
          lerp(riggedFace.mouth.shape.E, Blendshape.getValue(PresetName.E), 0.5)
        );
        Blendshape.setValue(
          PresetName.O,
          lerp(riggedFace.mouth.shape.O, Blendshape.getValue(PresetName.O), 0.5)
        );
        Blendshape.setValue(
          PresetName.U,
          lerp(riggedFace.mouth.shape.U, Blendshape.getValue(PresetName.U), 0.5)
        );

        //瞳孔
        //插值瞳孔并保留值的副本
        let lookTarget = new THREE.Euler(
          lerp(oldLookTarget.x, riggedFace.pupil.y, 0.4),
          lerp(oldLookTarget.y, riggedFace.pupil.x, 0.4),
          0,
          "XYZ"
        );
        oldLookTarget.copy(lookTarget);
        currentVrm.lookAt.applyer.lookAt(lookTarget);
      };

      ////////////////////////////
      /* VRM Character Animator */
      ////////////////////////////
      const animateVRM = (vrm, results) => {
        if (!vrm) {
          return;
        }
        // 从'holistic'中获取结果，并根据角色的面部、姿势和手部关键点为其设置动画
        let riggedPose, riggedLeftHand, riggedRightHand, riggedFace;

        const faceLandmarks = results.faceLandmarks;
        // 3d姿态 地标与髋部距离有关，单位为米
        const pose3DLandmarks = results.ea;
        // 2d姿态 地标与视频宽度和视频高度有关
        const pose2DLandmarks = results.poseLandmarks;
        // 注意，手部标志可能会颠倒
        const leftHandLandmarks = results.rightHandLandmarks;
        const rightHandLandmarks = results.leftHandLandmarks;

        // 脸部动画
        if (faceLandmarks) {
          riggedFace = Kalidokit.Face.solve(faceLandmarks, {
            runtime: "mediapipe",
            video: videoElement,
          });
          rigFace(riggedFace);
        }

        // 身体动画
        if (pose2DLandmarks && pose3DLandmarks) {
          riggedPose = Kalidokit.Pose.solve(pose3DLandmarks, pose2DLandmarks, {
            runtime: "mediapipe",
            video: videoElement,
          });
          rigRotation("Hips", riggedPose.Hips.rotation, 0.7);
          rigPosition(
            "Hips",
            {
              x: riggedPose.Hips.position.x, // Reverse direction
              y: riggedPose.Hips.position.y + 1, // Add a bit of height
              z: -riggedPose.Hips.position.z, // Reverse direction
            },
            1,
            0.07
          );

          rigRotation("Chest", riggedPose.Spine, 0.25, 0.3);
          rigRotation("Spine", riggedPose.Spine, 0.45, 0.3);

          rigRotation("RightUpperArm", riggedPose.RightUpperArm, 1, 0.3);
          rigRotation("RightLowerArm", riggedPose.RightLowerArm, 1, 0.3);
          rigRotation("LeftUpperArm", riggedPose.LeftUpperArm, 1, 0.3);
          rigRotation("LeftLowerArm", riggedPose.LeftLowerArm, 1, 0.3);

          rigRotation("LeftUpperLeg", riggedPose.LeftUpperLeg, 1, 0.3);
          rigRotation("LeftLowerLeg", riggedPose.LeftLowerLeg, 1, 0.3);
          rigRotation("RightUpperLeg", riggedPose.RightUpperLeg, 1, 0.3);
          rigRotation("RightLowerLeg", riggedPose.RightLowerLeg, 1, 0.3);
        }

        // 手部动画
        if (leftHandLandmarks) {
          riggedLeftHand = Kalidokit.Hand.solve(leftHandLandmarks, "Left");
          rigRotation("LeftHand", {
            // 组合姿势旋转Z和手旋转X Y
            z: riggedPose.LeftHand.z,
            y: riggedLeftHand.LeftWrist.y,
            x: riggedLeftHand.LeftWrist.x,
          });
          rigRotation("LeftRingProximal", riggedLeftHand.LeftRingProximal);
          rigRotation(
            "LeftRingIntermediate",
            riggedLeftHand.LeftRingIntermediate
          );
          rigRotation("LeftRingDistal", riggedLeftHand.LeftRingDistal);
          rigRotation("LeftIndexProximal", riggedLeftHand.LeftIndexProximal);
          rigRotation(
            "LeftIndexIntermediate",
            riggedLeftHand.LeftIndexIntermediate
          );
          rigRotation("LeftIndexDistal", riggedLeftHand.LeftIndexDistal);
          rigRotation("LeftMiddleProximal", riggedLeftHand.LeftMiddleProximal);
          rigRotation(
            "LeftMiddleIntermediate",
            riggedLeftHand.LeftMiddleIntermediate
          );
          rigRotation("LeftMiddleDistal", riggedLeftHand.LeftMiddleDistal);
          rigRotation("LeftThumbProximal", riggedLeftHand.LeftThumbProximal);
          rigRotation(
            "LeftThumbIntermediate",
            riggedLeftHand.LeftThumbIntermediate
          );
          rigRotation("LeftThumbDistal", riggedLeftHand.LeftThumbDistal);
          rigRotation("LeftLittleProximal", riggedLeftHand.LeftLittleProximal);
          rigRotation(
            "LeftLittleIntermediate",
            riggedLeftHand.LeftLittleIntermediate
          );
          rigRotation("LeftLittleDistal", riggedLeftHand.LeftLittleDistal);
        }
        if (rightHandLandmarks) {
          riggedRightHand = Kalidokit.Hand.solve(rightHandLandmarks, "Right");
          rigRotation("RightHand", {
            // 组合来自姿势手的Z轴和来自手腕旋转的X/Y轴
            z: riggedPose.RightHand.z,
            y: riggedRightHand.RightWrist.y,
            x: riggedRightHand.RightWrist.x,
          });
          rigRotation("RightRingProximal", riggedRightHand.RightRingProximal);
          rigRotation(
            "RightRingIntermediate",
            riggedRightHand.RightRingIntermediate
          );
          rigRotation("RightRingDistal", riggedRightHand.RightRingDistal);
          rigRotation("RightIndexProximal", riggedRightHand.RightIndexProximal);
          rigRotation(
            "RightIndexIntermediate",
            riggedRightHand.RightIndexIntermediate
          );
          rigRotation("RightIndexDistal", riggedRightHand.RightIndexDistal);
          rigRotation(
            "RightMiddleProximal",
            riggedRightHand.RightMiddleProximal
          );
          rigRotation(
            "RightMiddleIntermediate",
            riggedRightHand.RightMiddleIntermediate
          );
          rigRotation("RightMiddleDistal", riggedRightHand.RightMiddleDistal);
          rigRotation("RightThumbProximal", riggedRightHand.RightThumbProximal);
          rigRotation(
            "RightThumbIntermediate",
            riggedRightHand.RightThumbIntermediate
          );
          rigRotation("RightThumbDistal", riggedRightHand.RightThumbDistal);
          rigRotation(
            "RightLittleProximal",
            riggedRightHand.RightLittleProximal
          );
          rigRotation(
            "RightLittleIntermediate",
            riggedRightHand.RightLittleIntermediate
          );
          rigRotation("RightLittleDistal", riggedRightHand.RightLittleDistal);
        }
      };

      ////////////////////////////
      /* 设置 MEDIAPIPE 整体实例 */
      ////////////////////////////

      let videoElement = document.querySelector(".input_video"),
        guideCanvas = document.querySelector("canvas.guides");

      const onResults = (results) => {
        console.log(1);
        // 绘制地标参考线
        drawResults(results);
        // 设置模型动画
        animateVRM(currentVrm, results);
      };

      const holistic = new Holistic({
        locateFile: (file) => {
          console.log(file);
          return `static/holistic/${file}`;
        },
      });

      holistic.setOptions({
        modelComplexity: 1,
        smoothLandmarks: true,
        minDetectionConfidence: 0.7,
        minTrackingConfidence: 0.7,
        refineFaceLandmarks: true,
      });

      const drawResults = (results) => {
        guideCanvas.width = videoElement.videoWidth;
        guideCanvas.height = videoElement.videoHeight;
        let canvasCtx = guideCanvas.getContext("2d");
        canvasCtx.save();
        canvasCtx.clearRect(0, 0, guideCanvas.width, guideCanvas.height);
        // Use `Mediapipe` drawing functions
        drawConnectors(canvasCtx, results.poseLandmarks, POSE_CONNECTIONS, {
          color: "#00cff7",
          lineWidth: 4,
        });
        drawLandmarks(canvasCtx, results.poseLandmarks, {
          color: "#ff0364",
          lineWidth: 2,
        });
        drawConnectors(canvasCtx, results.faceLandmarks, FACEMESH_TESSELATION, {
          color: "#C0C0C070",
          lineWidth: 1,
        });
        if (results.faceLandmarks && results.faceLandmarks.length === 478) {
          //draw pupils
          drawLandmarks(
            canvasCtx,
            [results.faceLandmarks[468], results.faceLandmarks[468 + 5]],
            {
              color: "#ffe603",
              lineWidth: 2,
            }
          );
        }
        drawConnectors(canvasCtx, results.leftHandLandmarks, HAND_CONNECTIONS, {
          color: "#eb1064",
          lineWidth: 5,
        });
        drawLandmarks(canvasCtx, results.leftHandLandmarks, {
          color: "#00cff7",
          lineWidth: 2,
        });
        drawConnectors(
          canvasCtx,
          results.rightHandLandmarks,
          HAND_CONNECTIONS,
          {
            color: "#22c3e3",
            lineWidth: 5,
          }
        );
        drawLandmarks(canvasCtx, results.rightHandLandmarks, {
          color: "#ff0364",
          lineWidth: 2,
        });
      };

      // 传给holistic回调函数
      holistic.onResults(onResults);

      // 使用“Mediapipe”UTIL获取摄像机以及较低分辨率获得较高的帧频
      const camera = new Camera(videoElement, {
        onFrame: async () => {
          await holistic.send({ image: videoElement });
        },
        width: 3000,
        height: 3000,
      });
      camera.start();

      //拖拽
      this.move();

      //recode
      let canvas = document.querySelectorAll("canvas");
      let canvasList = Array.from(canvas);
      let animateCanvas = canvasList[1];
      let stream = animateCanvas.mozCaptureStream
        ? animateCanvas.mozCaptureStream(60)
        : animateCanvas.captureStream(60);
      let recorder = new MediaRecorder(stream, { mimeType: "video/webm" });

      recorder.onstop = () => {
        //结束录制时下载视频
        const url = URL.createObjectURL(
          new Blob(this.recodeData, { type: "video/webm" })
        );
        let element = document.createElement("a");
        element.setAttribute("href", url);
        element.setAttribute("download", "");
        element.style.display = "none";
        document.body.appendChild(element);
        element.click();
        document.body.removeChild(element);
      };

      recorder.ondataavailable = (e) => {
        if (e.data && e.data.size) {
          this.recodeData.push(e.data);
        }
      };

      let startBtn = document.getElementById("startBtn");
      let endBtn = document.getElementById("endBtn");

      startBtn.onclick = (e) => {
        if (this.ifRecoding === "true") return;
        startBtn.style.background = "rgba(100,100,100)";
        endBtn.style.background = "rgba(0,0,0)";
        startBtn.style.cursor = "not-allowed";
        endBtn.style.cursor = "pointer";
        recorder.start();
        console.log("开始录制");
      };

      endBtn.onclick = (e) => {
        if (this.ifRecoding === "flase") return;
        endBtn.style.background = "rgba(100,100,100)";
        startBtn.style.background = "rgba(0,0,0)";
        startBtn.style.cursor = "pointer";
        endBtn.style.cursor = "not-allowed";
        recorder.stop();
        this.recodeData = [];
        console.log("结束录制");
      };
    },
    comeIn() {
      this.ifCome = false;
      this.ifStart = true;
    },
    setup(e) {
      // 创建文件读取对象
      // console.log(1);
      var reader = new FileReader();

      //文件存储在file表单元素的files属性中，它是一个数组
      //没有返回值，但是读取完毕后，将读取结果存储在对象的result中
      var fil = document.getElementById("file").files;
      reader.readAsDataURL(fil[0]);

      let that = this;
      //当读取成功后触发
      reader.onload = (e) => {
        that.character = e.target.result;
        that.start();
      };
    },
    move() {
      let div = document.getElementById("preview");
      let ifMove = false;
      let position = null;
      div.addEventListener("mousedown", (e) => {
        ifMove = true;
        position = [e.clientX, e.clientY];
      });
      document.addEventListener("mousemove", (e) => {
        if (ifMove === false) return;
        let x = e.clientX;
        let y = e.clientY;
        let movedX = position[0] - x;
        let movedY = position[1] - y;
        let right = parseInt(div.style.right || 0);
        let bottom = parseInt(div.style.bottom || 0);
        div.style.right = right + movedX + "px";
        div.style.bottom = bottom + movedY + "px";
        position = [x, y];
      });
      document.addEventListener("mouseup", () => {
        ifMove = false;
      });
    },
  },
  watch: {
    visible(value) {
      if (value) {
        document.body.addEventListener("click", this.closeMenu);
      } else {
        document.body.removeEventListener("click", this.closeMenu);
      }
    },
  },
};
</script>>

<style lang="less" scoped>
#app {
  -webkit-user-seletct: none;
  -moz-user-seletct: none;
  overflow: hidden;
  /deep/ input::-webkit-input-placeholder {
    color: #fff;
  }
  .contextmenu {
    margin: 0;
    background: #fff;
    z-index: 3000;
    position: absolute;
    list-style-type: none;
    padding: 5px 0;
    border-radius: 4px;
    font-size: 12px;
    font-weight: 400;
    color: #333;
    box-shadow: 2px 2px 3px 0 rgba(0, 0, 0, 0.3);
  }

  .contextmenu li {
    margin: 0;
    padding: 7px 16px;
    cursor: pointer;
  }
  .contextmenu li:hover {
    background: #eee;
  }
  #svgA {
    position: fixed;
    left: 1vw;
    top: 1vw;
    z-index: 100;
    width: 2vw;
    height: 2vw;
    transition: all 0.6s;
  }
  #svgA:hover {
    transform: scale(1.4);
  }
  #refresh {
    position: fixed;
    left: 4vw;
    top: 4vw;
    z-index: 100;
    width: 2vw;
    height: 2vw;
    transition: all 0.6s;
  }
  #refresh:hover {
    transform: scale(1.4);
  }
  #github {
    position: absolute;
    width: 10vw;
    height: 10vw;
    top: -5vw;
    left: -5vw;
    z-index: 99;
    transform: rotate(45deg);
    background-color: black;
  }
  #cover {
    display: flex;
    font-size: 2vw;
    height: 100vh;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    h3 {
      cursor: pointer;
    }
  }
  #two {
    height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    align-content: center;
    #option {
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      .file {
        width: 20vw;
        height: 20vh;
        background-color: black;
        border-radius: 20px;
      }
      .left {
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        align-items: center;
        height: 20vh;
        width: 20vw;
        /deep/.el-input__inner {
          border: 1px solid black;
          background-color: black;
          color: white;
        }
        h1 {
          cursor: pointer;
        }
      }
      input[type="file"]::-webkit-file-upload-button {
        background-color: black;
        color: white;
        font-size: 2vw;
        padding: 1vw;
        width: 20vw;
        height: 20vh;
      }
    }
  }
  canvas {
    transform: scale(-1, 1);
    display: block;
    cursor: all-scroll;
  }
  #recode {
    #startBtn {
      width: 7vw;
      height: 6vh;
      background-color: black;
      position: fixed;
      right: 10vw;
      top: 2vh;
      border-radius: 10px;
      color: #fff;
      font-size: 1vw;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      cursor: pointer;
      svg {
        margin-right: 3px;
        width: 3vh;
        height: 3vh;
      }
    }
    #endBtn {
      width: 7vw;
      height: 6vh;
      background-color: rgba(100, 100, 100);
      position: fixed;
      right: 2vw;
      top: 2vh;
      border-radius: 10px;
      color: #fff;
      font-size: 1vw;
      display: flex;
      flex-direction: row;
      align-items: center;
      justify-content: center;
      cursor: not-allowed;
      svg {
        margin-right: 3px;
        width: 3vh;
        height: 3vh;
      }
    }
  }
  .preview {
    display: flex;
    flex-direction: column;
    position: absolute;
    bottom: 16px;
    right: 16px;
    overflow: hidden;
    border-radius: 8px;
    background: #222;
    .guides {
      position: absolute;
      bottom: 0;
      left: 0;
      height: auto;
      width: 100%;
      z-index: 1;
    }
    video {
      max-width: 400px;
      height: auto;
      transform: scale(-1, 1);
    }
  }
}
</style>
