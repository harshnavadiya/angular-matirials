#quotes project #sumitbhi #####



1)create angular project.


2)add matirial
		:--
			cmd 1:-- npm install --save @angular/material @angular/cdk
			cmd 2:-- 	npm install --save @angular/animations
									add in main module.ts
									import {BrowserAnimationsModule} from '@angular/platform-browser/animations';
									import {
											  MatAutocompleteModule,
											  MatButtonModule,
											  MatButtonToggleModule,
											  MatCardModule,
											  MatCheckboxModule,
											  MatChipsModule,
											  MatDatepickerModule,
											  MatDialogModule,
											  MatExpansionModule,
											  MatGridListModule,
											  MatIconModule,
											  MatInputModule,
											  MatListModule,
											  MatMenuModule,
											  MatNativeDateModule,
											  MatPaginatorModule,
											  MatProgressBarModule,
											  MatProgressSpinnerModule,
											  MatRadioModule,
											  MatRippleModule,
											  MatSelectModule,
											  MatSidenavModule,
											  MatSliderModule,
											  MatSlideToggleModule,
											  MatSnackBarModule,
											  MatSortModule,
											  MatTableModule,
											  MatTabsModule,
											  MatToolbarModule,
											  MatTooltipModule,
											  MatStepperModule,

											} from '@angular/material'; 
									 
									 
									 
									 
									 imports: [BrowserAnimationsModule,
									 MatAutocompleteModule,
											  MatButtonModule,
											  MatButtonToggleModule,
											  MatCardModule,
											  MatCheckboxModule,
											  MatChipsModule,
											  MatDatepickerModule,
											  MatDialogModule,
											  MatExpansionModule,
											  MatGridListModule,
											  MatIconModule,
											  MatInputModule,
											  MatListModule,
											  MatMenuModule,
											  MatNativeDateModule,
											  MatPaginatorModule,
											  MatProgressBarModule,
											  MatProgressSpinnerModule,
											  MatRadioModule,
											  MatRippleModule,
											  MatSelectModule,
											  MatSidenavModule,
											  MatSliderModule,
											  MatSlideToggleModule,
											  MatSnackBarModule,
											  MatSortModule,
											  MatTableModule,
											  MatTabsModule,
											  MatToolbarModule,
											  MatTooltipModule,
											  MatStepperModule,
									 
									 ],
								
							cmd 3:-- in style.css add line 
											
											@import "~@angular/material/prebuilt-themes/indigo-pink.css";
											
							cmd 4:-- npm install --save hammerjs
										in module.ts
												import 'hammerjs';
							
							cmd 5:-- add matirial icon 
										in index.html
										
										<link href="https://fonts.googleapis.com/icon?family=Material+Icons" rel="stylesheet">
										
4)install flex-layout
							cmd 1:--npm i @angular/flex-layout --save
							cmd 2:-- import in module.ts
										import { FlexLayoutModule } from '@angular/flex-layout';
										import:[FlexLayoutModule]
										
3) add other libraries
			like:-----
						import {FormsModule, ReactiveFormsModule} from '@angular/forms';
						import {Route,RouterModule} from '@angular/router';
						import { HttpModule } from '@angular/http';
						
						import:[
						  FormsModule,
							HttpModule,
							RouterModule
						]
4)careate routing :----

			ng g module web-routing
						
						open web-routing.ts
								1)add;
									import { Routes,RouterModule } from '@angular/router';
									const routes: Routes = [
  
															{

															path:'',
															component: BaseManagement
															},
															];
									import:[
									RouterModule.forRoot(routes)
									]
									
									now 
								2)add in app.module.ts
									import { WebRoutingModule } from './web-routing/web-routing.module';
									
									import:[
									WebRoutingModule

									];
								3)add app.component.html in remove all and add it
											<router-outlet></router-outlet>
									
						
5)add base component 
				cmd 1:--ng g component base-management
				now create deshboard view by those code:---
				
				
				1)html:----\
								<section class="app flex-container" fxLayout="column" fxLayoutAlign="start stretch">
								<!-- this flex item takes the rest of the screen in height -->
								<mat-sidenav-container fxFlex>

									<mat-sidenav #sidenav mode="side" opened class=" mat-elevation-z4" fxLayout="column">
										<div class="header-nav">
											<h1 align="center">Collage</h1>
										</div>
										<section class="flex-containers">
											<section class="flex-items">
												<mat-expansion-panel>
													<mat-expansion-panel-header>
														<mat-panel-title>
															<mat-icon class="md-18 example-icon">dashboard</mat-icon>
															<span>Dashboard</span>
														</mat-panel-title>
													</mat-expansion-panel-header>
												</mat-expansion-panel>

												<!-- <mat-expansion-panel>
												  <mat-expansion-panel-header>
													  <mat-panel-title>
														  <mat-icon class="md-18 example-icon" fxFlex>person</mat-icon>
														  <span>Teacher</span>
													  </mat-panel-title>
													  <mat-panel-description>
													  </mat-panel-description>
												  </mat-expansion-panel-header>
												  <mat-nav-list>
													  <mat-list-item>
														  <a matLine routerLink="/add-teacher" routerLinkActive="active">
															  <span>Add Teacher</span>
														  </a>
													  </mat-list-item>
												  </mat-nav-list>
												  <mat-nav-list>
													  <mat-list-item>
														  <a matLine routerLink="/teacher-list" routerLinkActive="active">
															  <span>Search Teacher</span>
														  </a>
													  </mat-list-item>
												  </mat-nav-list>
											  </mat-expansion-panel> -->

												
											</section>
										</section>
									</mat-sidenav>

									<section>
										<section class="data">
											<!-- <section class="flex-container"> -->

											<mat-toolbar class=" mat-elevation-z4">
												<button mat-icon-button (click)="sidenav.toggle()">
															  <mat-icon>menu</mat-icon>
													  </button>

												<span class="example-spacer"></span>


												<button mat-icon-button class="icon" (click)="logout()">
													  <mat-icon>power_settings_new</mat-icon>
													 
												  </button>

											</mat-toolbar>

										</section>

										<router-outlet></router-outlet>
									</section>


								</mat-sidenav-container>

							</section>

				2:------/ base-management.css
				
								body {
									padding: 0;
									margin: 0;
									font-family: Roboto, sans-serif;
								}

								.app {
									height: 97.9vh;
									overflow: auto;
								}

								.data {
									flex-direction: row;
									flex-flow: inherit;
									height: max-content;
								}

								mat-toolbar {
									background-color: rgb(90, 212, 206);
									z-index: 10;
									height: 50px;
								}

								button {
									outline: none;
								}

								mat-sidenav {
									flex-flow: nowrap;
									flex: 0 0 auto;
									overflow-y: auto;
									display: flex;
								}

								.z-depth-2 {
									box-shadow: 0 4px 5px 0 rgba(0, 0, 0, 0.14), 0 1px 10px 0 rgba(0, 0, 0, 0.12), 0 2px 4px -1px rgba(0, 0, 0, 0.3);
									z-index: 15000;
								}

								.example-spacer {
									flex: 1 1 auto;
								}

								.example-icon {
									padding-right: 5px;
								}

								a {
									text-decoration-color: black;
									text-decoration-line: none;
									-webkit-text-fill-color: black;
								}

								.flex-item {
									flex: 1 1 auto;
									align-self: auto;
									width: calc(100% - 10px);
									padding: 10px;
									padding-right: 2px
								}

								.flex-items {
									flex: 1 1 auto;
									align-self: auto;
									width: calc(100% - 10px);
									padding: 5px;
								}

								.flex-containers {
									display: flex;
									flex-direction: row;
									flex-wrap: nowrap;
									justify-content: flex-start;
									align-content: stretch;
									align-items: flex-start;
									padding: 10px;
									height: max-content;
								}

								.cont {
									background-color: white;
								}

								.hei {
									height: 100%
								}

								mat-sidenav {
									overflow: hidden;
								}

								mat-sidenav:hover {
									overflow-y: scroll;
								}

								.header-nav {
									background-color: rgb(90, 212, 206);
								}

			now 
					ng serve 
					
6)now we make sidebar 

					add in basemanagementcomponent.html
					
						<mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>

                                <mat-icon class="md-18 example-icon" fxFlex>notifications_paused</mat-icon>
                                <span>Push Notification</span>

                            </mat-panel-title>
                            <mat-panel-description>
                            </mat-panel-description>
                        </mat-expansion-panel-header>
                        <mat-nav-list>
                            <mat-list-item>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <span>Status</span>
                                </a>
                            </mat-list-item>
                        </mat-nav-list>
                        <mat-nav-list>
                            <mat-list-item>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <span>Catagory</span>
                                </a>
                            </mat-list-item>
                        </mat-nav-list>
                        <mat-nav-list>
                            <mat-list-item>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <span>Url</span>
                                </a>
                            </mat-list-item>
                        </mat-nav-list>
                    </mat-expansion-panel>
                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="view_module">dashboard</mat-icon>
                                    <span>Catagory</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>
                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="assignment_turned_in">dashboard</mat-icon>
                                    <span>Status to review</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>

                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="flag">dashboard</mat-icon>
                                    <span>Languages</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>

                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="comment">dashboard</mat-icon>
                                    <span>Comments</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>

                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="message">dashboard</mat-icon>
                                    <span>Support Massages</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>

                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="apps">dashboard</mat-icon>
                                    <span>Version App</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>

                    <mat-expansion-panel>
                        <mat-expansion-panel-header>
                            <mat-panel-title>
                                <a matLine routerLink="/" routerLinkActive="active">
                                    <mat-icon class="people">dashboard</mat-icon>
                                    <span>User</span>
                                </a>
                            </mat-panel-title>
                        </mat-expansion-panel-header>
                    </mat-expansion-panel>
					
7)now make dashboard dashboard	
					to access shortly admin panal
					cmd 1:-- make active title
					
							make class comman
									ng g class common
									
							now add this common code in it:---
							
										//fixed memory adderss to we use static keyword
										 public static isDev = true;
										 public static baseUrl = 'http://localhost:3000/api';
										 public static socketBaseUrl = 'http://localhost:3000';
										 public static imageUrl = 'http://localhost:3000/img';


										 //user ID
										 public static user_id= localStorage.getItem('user_id');

										//login
										 public static sv_login_user='/login';

										 static Dlog(object: any) {
											 if (Common.isDev) {
												 console.log(object);
											 }
										 }

										 //roottitle Display
										 activeroot:string="Dashboard";

										   //socket update 
										   public static sv_update_socket='UpdateSocket';
											and assign root form component onit method.
											
					cmd 2:--- now make disgin of dashboard so cretate dashvoad component  
										ng g component dashboard
										
										and add routing children in web-routing.module.ts as follow:----
										
											  children: [{
															path:'',
															component:DashboardComponent
														  }];
														  
					cmd 3:---
							Add garphics code in dashboard.html
									<section class="flex-container">
										<section class="flex-item">
											<div fxLayout="row wrap" fxLayoutAlign="space-between start" style="margin-top:20px;margin-left: 20px;">

												<mat-card class="dashcard mat-elevation-z4">

													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>subtitles</mat-icon>
														</mat-card>
														<mat-card-header>

															<mat-card-title>Status
																<hr>
															</mat-card-title>

															<mat-card-subtitle>192</mat-card-subtitle>

														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>access_time</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Reviews
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>insert_comment</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Comments
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>view_list</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Categoryies
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>people</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>users
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>flag</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Languages
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>devices_other</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Installs
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>help</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Supports
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>
												<mat-card class="dashcard mat-elevation-z4">
													<a matLine routerLink="/" routerLinkActive="active">
														<mat-card class="inner-card">
															<mat-icon>error</mat-icon>
														</mat-card>
														<mat-card-header>
															<mat-card-title>Version
																<hr>
															</mat-card-title>
															<mat-card-subtitle>192</mat-card-subtitle>
														</mat-card-header>
													</a>
												</mat-card>


											</div>
											<!-- // mat-elevation-z4 -->
										</section>
									</section>
									
									and css file code is :----
									
									.dashcard {
											width: 25%;
											height: 20%;
											margin: 10px;
										}

										.dashcard:hover {
											box-shadow: 0 2px 8px -1px rgba(0, 0, 0, .2), 0 8px 5px 0 rgba(0, 0, 0, .14), 0 1px 10px 0 rgba(0, 0, 0, .12);
										}

										.inner-card {
											width: 30px;
											height: 30px;
											float: left;
											background: linear-gradient(60deg, #222a97, #325ccf);
										}

										mat-card-header {
											float: right;
										}

										mat-card-subtitle {
											font-size: 30px;
										}

										mat-card-title {
											font-size: 30px;
										}

										mat-icon {
											color: white;
											font-size: 30px;
										}
												
									End
									
8)Now we make a new status component to status
										cmd 1:-=-
												ng g component status-management
												
										cmd 2:- add html content:--
													<section class="flex-container" fxLayout="row wrap" fxLayoutAlign="space-between center">
														<section class="flex-item">
															<section align="center" fxLayout="row" fxLayoutAlign="space-around center">
																<button mat-raised-button disabled><mat-icon>format_quote</mat-icon>199 Status </button>

																<button mat-raised-button color="primary"><mat-icon>add</mat-icon> New Status  </button>
															</section>

														</section>
														<section class="flex-item">
															<mat-card class="example-card">
																<mat-card-header>
																	<div mat-card-avatar class="example-header-image"></div>
																	<mat-card-title>Shiba Inu</mat-card-title>
																	<mat-card-subtitle>Dog Breed</mat-card-subtitle>
																</mat-card-header>

																<mat-card-content class="status mat-elevation-z1">
																	<p>Hello its amazing wab</p>
																</mat-card-content>
																<mat-card-actions align="center">
																	<button mat-button color="primary"> <mat-icon>remove_red_eye</mat-icon></button>
																	<button mat-button color="accent"><mat-icon>edit</mat-icon></button>
																	<button mat-button color="warn"><mat-icon>close</mat-icon></button>
																	<button mat-button color="primary"><mat-icon>notifications_active</mat-icon></button>
																</mat-card-actions>
															</mat-card>
														</section>
													</section>
													
										cmd 3:-- now add css content:----
														.flex-item {
																	flex: 1 1 auto;
																	align-self: auto;
																	width: calc(100% - 10px);
																	padding: 10px;
																	padding-right: 2px
																}

																.flex-container {
																	display: flex;
																	flex-direction: row;
																	flex-wrap: nowrap;
																	justify-content: flex-start;
																	align-content: stretch;
																	align-items: flex-start;
																	padding: 10px;
																	height: max-content;
																}

																.example-card {
																	max-width: 400px;
																}

																.example-header-image {
																	background-image: url('https://material.angular.io/assets/img/examples/shiba1.jpg');
																	background-size: cover;
																}

																.status {
																	padding: 10px;
																	border-radius: 5px;
																}
										cmd 4:---
													now make its add status part :--
															
															cmd a:- ng g component status-management/status-add-management
															cmd b:-<section class="flex-container">
																		<section class="flex-item">
																			<section>
																				<H2>Status / Add Status </H2>
																				<section class="formcontain mat-elevation-z4">

																					<form class="example-form">

																						<section>
																							<mat-form-field style="width:100%">
																								<textarea matInput placeholder="Status content"></textarea>
																							</mat-form-field>
																						</section>

																						<section>
																							<h2>Status Background</h2>

																						</section>

																						<section>
																							<mat-checkbox color="primary">Enable Comment</mat-checkbox>
																						</section>

																						<!-- <mat-color-picker></mat-color-picker> -->
																						<section>
																							<mat-checkbox color="primary">Enabled</mat-checkbox>
																						</section>
																						<section>
																							<h2>Catagorys:</h2>
																							<section fxLayout="row wrap" fxLayoutAlign="space-around start">
																								<mat-checkbox color="primary" style="margin-left:-20px;">Love</mat-checkbox>
																								<mat-checkbox color="primary">Religion</mat-checkbox>
																								<mat-checkbox color="primary">Funny</mat-checkbox>
																								<mat-checkbox color="primary">Sad</mat-checkbox>
																								<mat-checkbox color="primary">Motivation</mat-checkbox>
																								<mat-checkbox color="primary">Work</mat-checkbox>
																								<mat-checkbox color="primary">Celebration</mat-checkbox>
																								<mat-checkbox color="primary">Sports</mat-checkbox>
																								<mat-checkbox color="primary">Legends</mat-checkbox>
																								<mat-checkbox color="primary">Countries</mat-checkbox>
																								<mat-checkbox color="primary">Foods</mat-checkbox>
																							</section>
																						</section>
																						<section>
																							<h2>Languages:</h2>
																							<section fxLayout="row">
																								<mat-checkbox color="primary" style="margin-right: 20px;">English</mat-checkbox>
																								<mat-checkbox color="primary" style="margin-right: 20px;">Hindi-हिंदी</mat-checkbox>
																								<mat-checkbox color="primary" style="margin-right: 20px;"> َArabic - العربية</mat-checkbox>

																							</section>
																						</section>
																						<section style="margin-top:20px;float:right" fxLayout="row">
																							<button mat-raised-button color="warn" style="margin-right: 50px;">
																									Cancel
																							</button>
																							<button mat-raised-button color="primary">
																								Save
																							</button>
																						</section>

																					</form>

																				</section>
																			</section>
																		</section>
																	</section>
																	
																	
															cmd c:--
																	add in css content:------#
																	
																	.flex-item {
																			flex: 1 1 auto;
																			align-self: auto;
																			width: calc(100% - 10px);
																			padding: 10px;
																			padding-right: 2px
																		}

																		.flex-container {
																			display: flex;
																			flex-direction: row;
																			flex-wrap: nowrap;
																			justify-content: flex-start;
																			align-content: stretch;
																			align-items: flex-start;
																			padding: 10px;
																			height: max-content;
																		}

																		.formcontain {
																			margin: 50px 80px;
																			border-radius: 5px;
																			padding: 50px;
																		}

																		.example-form {
																			margin: 20px;
																		}

										cmd 5:----
													
														add now add edit part same as add but just change some minor changes.
														
														
6)after it make catagory component 
										cmd 1:----
													ng g component categories-management
										cmd 2:--
													After it make html code and css 
										cmd 3:--
													And then add routing path 
													
7)Now create language component
										cmd 1:---
													ng g component language-management
													
													
													clsss:before{
													    position: absolute;
														top: 26px;
														right: -15px;
														display: inline-block;
														border-top: 15px solid transparent;
														border-left: 15px solid #e4e4e4;
														border-right: 0 solid #e4e4e4;
														border-bottom: 15px solid transparent;
														content: " ";
													}
													
8)now make a new comment component 
										cmd 1:----
													ng g component comment-management
													
9)now let we make image upload or file upload
									
									cmd:- 	1:--
													npm install ng2-file-upload --save
													
									cmd:- 2:--
														import { FileSelectDirective } from 'ng2-file-upload';
														declarations: [
															
															FileSelectDirective
														  ],
														  
									cmd 3:---
													import {  FileUploader, FileSelectDirective } from 'ng2-file-upload/ng2-file-upload';

													const URL = 'http://localhost:3000/api/upload';
													
													
													  public uploader: FileUploader = new FileUploader({url: URL, itemAlias: 'photo'});

													   ngOnInit() {

																this.uploader.onAfterAddingFile = (file) => { file.withCredentials = false; };
																this.uploader.onCompleteItem = (item: any, response: any, status: any, headers: any) => {
																	 console.log('ImageUpload:uploaded:', item, status, response);
																	 alert('File uploaded successfully');
																 };
															  }
									cmd 4:-- in node js in controlers add this code:--
									const path = require('path');

									const multer = require('multer');
														const DIR = './uploads';
																		 
																		let storage = multer.diskStorage({
																			destination: (req, file, cb) => {
																			  cb(null, DIR);
																			},
																			filename: (req, file, cb) => {
																			  cb(null, file.fieldname + '-' + Date.now() + '.' + path.extname(file.originalname));
																			}
																		});
																		let upload = multer({storage: storage});

																	
															

													app.get('/api', function (req, res) {
													  res.end('file catcher example');
													});
													 
													app.post('/api/upload',upload.single('photo'), function (req, res) {
														if (!req.file) {
															console.log("No file received");
															return res.send({
															  success: false
															});
														
														  } else {
															console.log('file received');
															return res.send({
															  success: true
															})
														  }
													});
																											
 
10)make a login screen
					
						cmd:1----
									ng g component login-management
	
						cmd 2:----
									write in .html file
									
									<div class="data-view">
    <div calss="card">
        <div calss="card-block m-t-35">
            <h1 align="center" style="padding-top:10%;color:white">School</h1>
            <div fxLayout="column" fxLayoutAlign="center center" fxLayoutGap="10px">
                <form class="example-form">


                    <div fxLayout="column" fxLayoutAlign="center center" class="data-container  mat-elevation-z4">

                        <mat-icon matInfix>lock</mat-icon>
                        <h2><strong>Login</strong> to your account</h2>

                        <mat-form-field fxFlex="1 1 auto" style="width: 90%">
                            <mat-icon matPrefix>perm_identity</mat-icon>
                            <input matInput placeholder="User Name" [(ngModel)]="user_name" name="service_name">
                        </mat-form-field>


                        <mat-form-field fxFlex="1 1 auto" style="width: 90%">
                            <mat-icon matPrefix>lock_outline</mat-icon>
                            <input matInput type="password" placeholder="Password" [(ngModel)]="password" name="service_name">
                        </mat-form-field>

                        <div class="animf">
                            <button mat-raised-button color="primary" (click)="login()">Login</button>
                        </div>
                    </div>

                </form>


            </div>
        </div>
    </div>
</div>

					cmd 2:----
					
						.data-container {
    display: flex;
    padding: 10px;
    overflow: hidden;
    border-radius: 5px;
    width: 500px;
    background-color: #fefefe;
    overflow: hidden;
}

.data-view {
    width: auto;
    height: auto;
    /* background-color: rgb(90, 212, 206); */
    padding-bottom: 14.5%;
    margin: 0;
}

					cmd 3:--
							Add in .ts file this.
							
							import { Component, OnInit } from '@angular/core';
import { Http } from '@angular/http';
import { WebServiceService } from '../web-service.service';
import { ActivatedRoute, Router } from '@angular/router';
import { MatSnackBar } from '@angular/material';
import { Common } from '../common';

@Component({
  selector: 'app-login-management',
  templateUrl: './login-management.component.html',
  styleUrls: ['./login-management.component.css']
})
export class LoginManagementComponent implements OnInit {
  user_name:string="";
  password:string="";
  returnUrl: string;
  constructor(private http:Http,private webService:WebServiceService,private route: ActivatedRoute , private router: Router,public snackBar: MatSnackBar) { }

  openMessage(message: string) {
    this.snackBar.open(message, 'Ok', {
      duration: 2000
    });
  }

  login(){
    //call to login service and pass data in service throu backand
    this.webService.webAction(Common.sv_login_user,{'email':this.user_name,'password':this.password})
    .then(responseObj => {
      Common.Dlog(responseObj);
      Common.Dlog(JSON.stringify(responseObj.payload[0].user_id));
      if (responseObj.status === 1 ) {
        //store useID
        localStorage.setItem('user_id', JSON.stringify(responseObj.payload[0].user_id));
       //change page
        this.router.navigate([this.returnUrl]);
        this.openMessage(responseObj.message);
    } else {
      this.openMessage(responseObj.message);
    }
      
    })
    .catch((err) => Common.Dlog(err))
  }


  ngOnInit() {

    this.returnUrl = this.route.snapshot.queryParams['returnUrl'] || '/';

  }

}




							
									 


