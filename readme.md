# Importation du projet dans Xamarin avec un projet Java Binding

## Fichier Metadata.xml

	<attr path="/api/package[@name='com.artifex.mupdfdemo']/class[@name='ArrayDeque.AscendingDequeIterator']/method[@name='next']" name="return">Java.Lang.Object</attr>

	<attr path="/api/package[@name='com.artifex.mupdfdemo']/class[@name='ArrayDeque.DescendingDequeIterator']/method[@name='next']" name="return">Java.Lang.Object</attr>

## Fichier PartialClasses.cs

	using Android.Runtime;

	namespace Com.Artifex.Mupdfdemo
	{
	    partial class ReaderView
	    {
	        protected override Java.Lang.Object RawAdapter
	        {
	            get { return Adapter.JavaCast<Java.Lang.Object>(); }
	            set { Adapter = value.JavaCast<global::Android.Widget.IListAdapter>(); }
	        }
	    }
	}