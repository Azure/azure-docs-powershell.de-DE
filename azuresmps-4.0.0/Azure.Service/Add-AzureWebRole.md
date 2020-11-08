---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FB5CD696-108D-4A3E-8983-1C6562E8795A
online version: ''
schema: 2.0.0
ms.openlocfilehash: 25ade8ccf395d37ab0856742fe473a6508c9d63b
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005917"
---
# <span data-ttu-id="f1aab-101">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="f1aab-101">Add-AzureWebRole</span></span>

## <span data-ttu-id="f1aab-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f1aab-102">SYNOPSIS</span></span>
<span data-ttu-id="f1aab-103">Fügt eine Web Worker-Rolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="f1aab-103">Adds a web worker role.</span></span>

## <span data-ttu-id="f1aab-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f1aab-104">SYNTAX</span></span>

```
Add-AzureWebRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1aab-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f1aab-105">DESCRIPTION</span></span>
<span data-ttu-id="f1aab-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="f1aab-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="f1aab-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="f1aab-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="f1aab-108">Das **Add-AzureWebRole-** Cmdlet fügt eine Web Worker-Rolle hinzu.</span><span class="sxs-lookup"><span data-stu-id="f1aab-108">The **Add-AzureWebRole** cmdlet adds a web worker role.</span></span>

## <span data-ttu-id="f1aab-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f1aab-109">EXAMPLES</span></span>

### <span data-ttu-id="f1aab-110">Beispiel 1: Hinzufügen einer Standardrolle</span><span class="sxs-lookup"><span data-stu-id="f1aab-110">Example 1: Add a default role</span></span>
```
PS C:\> Add-AzureWebRole
```

<span data-ttu-id="f1aab-111">Dieser Befehl Add Web Role mit der Standardkonfiguration von Webrole1 als Name und einer einzelnen Instanz.</span><span class="sxs-lookup"><span data-stu-id="f1aab-111">This command add web role that has the default configuration of Webrole1 as the name and a single instance.</span></span>

### <span data-ttu-id="f1aab-112">Beispiel 2: Hinzufügen einer Rolle mit einem Namen</span><span class="sxs-lookup"><span data-stu-id="f1aab-112">Example 2: Add a role with a name</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole"
```

<span data-ttu-id="f1aab-113">Mit diesem Befehl wird der aktuellen Anwendung eine einzelne webrolle mit dem Namen "MyWebRole" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1aab-113">This command adds a single web role named MyWebRole to the current application.</span></span>

### <span data-ttu-id="f1aab-114">Beispiel 3: Hinzufügen einer Rolle mit einem Namen und einer instanzenanzahl</span><span class="sxs-lookup"><span data-stu-id="f1aab-114">Example 3: Add a role with a name and instance count</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -Instance 2
```

<span data-ttu-id="f1aab-115">Mit diesem Befehl wird der aktuellen Anwendung eine webrolle mit dem Namen "MyWebRole" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1aab-115">This command adds a web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="f1aab-116">Das Cmdlet weist eine Rolleninstanzen Anzahl von 2 auf.</span><span class="sxs-lookup"><span data-stu-id="f1aab-116">The cmdlet has a role instance count of 2.</span></span>

### <span data-ttu-id="f1aab-117">Beispiel 4: Hinzufügen einer Rolle mit einem Namen und einer Vorlage</span><span class="sxs-lookup"><span data-stu-id="f1aab-117">Example 4: Add a role with a name and template</span></span>
```
PS C:\> Add-AzureWebRole -Name "MyWebRole" -TemplateFolder ".\MyWebTemplateFolder"
```

<span data-ttu-id="f1aab-118">Mit diesem Befehl wird der aktuellen Anwendung eine einzelne webrolle mit dem Namen "MyWebRole" hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1aab-118">This command adds a single web role named MyWebRole to the current application.</span></span>
<span data-ttu-id="f1aab-119">Der Befehl gibt einen Ordner mit dem Namen "MyWebTemplateFolder" als Gerüst Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="f1aab-119">The command specifies a folder named MyWebTemplateFolder as a scaffolding template.</span></span>

## <span data-ttu-id="f1aab-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="f1aab-120">PARAMETERS</span></span>

### <span data-ttu-id="f1aab-121">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="f1aab-121">-Instances</span></span>
<span data-ttu-id="f1aab-122">Gibt die Anzahl der Instanzen an.</span><span class="sxs-lookup"><span data-stu-id="f1aab-122">Specifies the number of instances.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: i

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1aab-123">-Name</span><span class="sxs-lookup"><span data-stu-id="f1aab-123">-Name</span></span>
<span data-ttu-id="f1aab-124">Gibt den Namen der webrolle an.</span><span class="sxs-lookup"><span data-stu-id="f1aab-124">Specifies the name of the web role.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: n

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1aab-125">-Profil</span><span class="sxs-lookup"><span data-stu-id="f1aab-125">-Profile</span></span>
<span data-ttu-id="f1aab-126">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="f1aab-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="f1aab-127">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="f1aab-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="f1aab-128">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="f1aab-128">-TemplateFolder</span></span>
<span data-ttu-id="f1aab-129">Gibt den Vorlagenordner an.</span><span class="sxs-lookup"><span data-stu-id="f1aab-129">Specifies the template folder.</span></span>

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

### <span data-ttu-id="f1aab-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1aab-130">CommonParameters</span></span>
<span data-ttu-id="f1aab-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f1aab-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1aab-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1aab-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1aab-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f1aab-133">INPUTS</span></span>

## <span data-ttu-id="f1aab-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f1aab-134">OUTPUTS</span></span>

## <span data-ttu-id="f1aab-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="f1aab-135">NOTES</span></span>

## <span data-ttu-id="f1aab-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f1aab-136">RELATED LINKS</span></span>

[<span data-ttu-id="f1aab-137">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="f1aab-137">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)

[<span data-ttu-id="f1aab-138">Neu – AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="f1aab-138">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


