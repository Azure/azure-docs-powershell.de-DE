---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 3B3F1870-348D-4303-9520-FD81D4650F5F
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2103a155b12fdf1e481173d529ff3308a3b2200b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006718"
---
# <span data-ttu-id="5c099-101">Get-AzureWebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="5c099-101">Get-AzureWebHostingPlan</span></span>

## <span data-ttu-id="5c099-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5c099-102">SYNOPSIS</span></span>
<span data-ttu-id="5c099-103">Ruft Azure Web Hosting-Pläne im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-103">Gets Azure web hosting plans in the current subscription.</span></span>

## <span data-ttu-id="5c099-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5c099-104">SYNTAX</span></span>

```
Get-AzureWebHostingPlan [-WebSpaceName <String>] [-Name <String>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="5c099-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5c099-105">DESCRIPTION</span></span>
<span data-ttu-id="5c099-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5c099-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5c099-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5c099-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5c099-108">Das Cmdlet " **Get-AzureWebHostingPlan** " Ruft die Azure Web Hosting-Pläne im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-108">The **Get-AzureWebHostingPlan** cmdlet gets the Azure web hosting plans in the current subscription.</span></span>

<span data-ttu-id="5c099-109">Standardmäßig ruft **Get-AzureWebHostingPlan** alle Azure-hostpläne im aktuellen Abonnement ab und gibt ein Objekt zurück, das grundlegende Informationen zu den Plänen bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5c099-109">By default, **Get-AzureWebHostingPlan** gets all Azure hosting plans in the current subscription and returns an object that provides basic information about the plans.</span></span>
<span data-ttu-id="5c099-110">Wenn Sie die Parameter *Webspace* und *Name* verwenden, gibt **Get-AzureWebHostingPlan** ein bestimmtes Host Planobjekt zurück.</span><span class="sxs-lookup"><span data-stu-id="5c099-110">When you use the *WebSpace* and *Name* parameters, **Get-AzureWebHostingPlan** returns a specific hosting plan object.</span></span>

<span data-ttu-id="5c099-111">Um das aktuelle Abonnement zu finden, verwenden Sie den *aktuellen* Parameter des Cmdlets **Get-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="5c099-111">To find the current subscription, use the *Current* parameter of the **Get-AzureSubscription** cmdlet.</span></span>
<span data-ttu-id="5c099-112">Wenn Sie das aktuelle Abonnement ändern möchten, verwenden Sie das Cmdlet **Select-AzureSubscription** .</span><span class="sxs-lookup"><span data-stu-id="5c099-112">To change the current subscription, use the **Select-AzureSubscription** cmdlet.</span></span>

## <span data-ttu-id="5c099-113">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5c099-113">EXAMPLES</span></span>

### <span data-ttu-id="5c099-114">Beispiel 1: Abrufen aller Webhosting-Pläne in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="5c099-114">Example 1: Get all web hosting plans in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan 

Name : Default1 
SKU : Basic 
WorkerSize : Small 
NumberOfWorkers : 1 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 1 
Status : Ready 
WebSpace : eastuswebspace 
Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready
```

<span data-ttu-id="5c099-115">Dieser Befehl ruft alle Azure Web Hosting-Pläne im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-115">This command gets all Azure web hosting plans in the current subscription.</span></span>

### <span data-ttu-id="5c099-116">Beispiel 2: Abrufen eines bestimmten Webhosting-Plans in einem Abonnement</span><span class="sxs-lookup"><span data-stu-id="5c099-116">Example 2: Get a specific web hosting plan in a subscription</span></span>
```
PS C:\> Get-AzureWebHostingPlan -WebSpaceName "westeuropewebspace" -Name "Default0" 

Name : Default0 
SKU : Free 
WorkerSize : Small 
NumberOfWorkers : 0 
CurrentWorkerSize : Small 
CurrentNumberOfWorkers : 0 
Status : Ready 
WebSpace : westeuropewebspace
```

<span data-ttu-id="5c099-117">Dieser Befehl ruft den Webhosting-Plan mit dem Namen Default0 im Webspace mit dem Namen westeuropewebspace im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-117">This command gets the web hosting plan named Default0 in the webspace named westeuropewebspace in the current subscription.</span></span>

## <span data-ttu-id="5c099-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="5c099-118">PARAMETERS</span></span>

### <span data-ttu-id="5c099-119">-Name</span><span class="sxs-lookup"><span data-stu-id="5c099-119">-Name</span></span>
<span data-ttu-id="5c099-120">Gibt den Namen eines Plans im Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="5c099-120">Specifies the name of a plan in the subscription.</span></span>
<span data-ttu-id="5c099-121">Standardmäßig ruft dieses Cmdlet alle Pläne im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-121">By default, this cmdlet gets all plans in the current subscription.</span></span>
<span data-ttu-id="5c099-122">Dieser Parameter unterstützt keine Platzhalterzeichen.</span><span class="sxs-lookup"><span data-stu-id="5c099-122">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c099-123">-Profil</span><span class="sxs-lookup"><span data-stu-id="5c099-123">-Profile</span></span>
<span data-ttu-id="5c099-124">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5c099-124">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5c099-125">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5c099-125">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c099-126">-Webspacename</span><span class="sxs-lookup"><span data-stu-id="5c099-126">-WebSpaceName</span></span>
<span data-ttu-id="5c099-127">Gibt den Namen eines Webspaces im Abonnement an.</span><span class="sxs-lookup"><span data-stu-id="5c099-127">Specifies the name of a webspace in the subscription.</span></span>
<span data-ttu-id="5c099-128">Standardmäßig ruft dieses Cmdlet alle Websites im angegebenen Webspace ab.</span><span class="sxs-lookup"><span data-stu-id="5c099-128">By default, this cmdlet gets all websites in the specified webspace.</span></span>
<span data-ttu-id="5c099-129">Dieser Parameter unterstützt keine Platzhalterzeichen.</span><span class="sxs-lookup"><span data-stu-id="5c099-129">This parameter does not support wildcard characters.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebSpace

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c099-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c099-130">CommonParameters</span></span>
<span data-ttu-id="5c099-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5c099-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c099-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5c099-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c099-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5c099-133">INPUTS</span></span>

###  
<span data-ttu-id="5c099-134">Sie können die Eingabe an dieses Cmdlet nach Eigenschaftsname, aber nicht nach Wert übergeben.</span><span class="sxs-lookup"><span data-stu-id="5c099-134">You can pass input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="5c099-135">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5c099-135">OUTPUTS</span></span>

### <span data-ttu-id="5c099-136">Microsoft. WindowsAzure. Commands. Utilities. Websites. Services. webentities. WebHostingPlan</span><span class="sxs-lookup"><span data-stu-id="5c099-136">Microsoft.WindowsAzure.Commands.Utilities.Websites.Services.WebEntities.WebHostingPlan</span></span>
<span data-ttu-id="5c099-137">Standardmäßig gibt **Get-AzureWebHostingPlan** ein Array von **WebHostingPlan** -Objekten zurück.</span><span class="sxs-lookup"><span data-stu-id="5c099-137">By default, **Get-AzureWebHostingPlan** returns an array of **WebHostingPlan** objects.</span></span>

## <span data-ttu-id="5c099-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="5c099-138">NOTES</span></span>

## <span data-ttu-id="5c099-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5c099-139">RELATED LINKS</span></span>

