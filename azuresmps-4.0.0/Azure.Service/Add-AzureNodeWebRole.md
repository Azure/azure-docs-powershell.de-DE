---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: C2DAFB2C-A58B-406C-8349-8728771B279E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 59aef29c27d7eb96834d270c2fce48ff3acb9554
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006598"
---
# <span data-ttu-id="5d02c-101">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="5d02c-101">Add-AzureNodeWebRole</span></span>

## <span data-ttu-id="5d02c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5d02c-102">SYNOPSIS</span></span>
<span data-ttu-id="5d02c-103">Erstellt erforderliche Dateien und Ordner für eine Node.js Anwendung.</span><span class="sxs-lookup"><span data-stu-id="5d02c-103">Creates required files and folders for a Node.js application.</span></span>

## <span data-ttu-id="5d02c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5d02c-104">SYNTAX</span></span>

```
Add-AzureNodeWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="5d02c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5d02c-105">DESCRIPTION</span></span>
<span data-ttu-id="5d02c-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="5d02c-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="5d02c-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="5d02c-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="5d02c-108">Das **Add-AzureNodeWebRole** erstellt erforderliche Dateien und Ordner, manchmal auch als Gerüst bezeichnet, damit eine Node.js Anwendung in der Cloud über IIS gehostet werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d02c-108">The **Add-AzureNodeWebRole** creates required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via IIS.</span></span>

## <span data-ttu-id="5d02c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5d02c-109">EXAMPLES</span></span>

### <span data-ttu-id="5d02c-110">Beispiel 1: webrolle einer einzelnen Instanz</span><span class="sxs-lookup"><span data-stu-id="5d02c-110">Example 1: Single instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole -Name MyWebRole
```

<span data-ttu-id="5d02c-111">In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne webrolle mit dem Namen " **MyWebRole** " hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="5d02c-111">This example adds scaffolding for a single web role named **MyWebRole** to the current application.</span></span>

### <span data-ttu-id="5d02c-112">Beispiel 2: webrolle für mehrere Instanzen</span><span class="sxs-lookup"><span data-stu-id="5d02c-112">Example 2: Multiple instance web role</span></span>
```
PS C:\> Add-AzureNodeWebRole MyWebRole -I 2
```

<span data-ttu-id="5d02c-113">In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine neue webrolle mit dem Namen **MyWebRole** hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="5d02c-113">This example adds scaffolding for a new web role named **MyWebRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="5d02c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5d02c-114">PARAMETERS</span></span>

### <span data-ttu-id="5d02c-115">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="5d02c-115">-Instances</span></span>
<span data-ttu-id="5d02c-116">Gibt die Anzahl der Rolleninstanzen für diese webrolle an.</span><span class="sxs-lookup"><span data-stu-id="5d02c-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="5d02c-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="5d02c-117">The default is 1.</span></span>

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

### <span data-ttu-id="5d02c-118">-Name</span><span class="sxs-lookup"><span data-stu-id="5d02c-118">-Name</span></span>
<span data-ttu-id="5d02c-119">Gibt den Namen der webrolle an.</span><span class="sxs-lookup"><span data-stu-id="5d02c-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="5d02c-120">Außerdem wird der Name des Verzeichnisses bestimmt, das das Gerüst für die node.js-Anwendung enthält, die in der webrolle gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="5d02c-120">It also determines the name of the directory that contains the scaffolding for the node.js application that will be hosted in the web role.</span></span>
<span data-ttu-id="5d02c-121">Der Standardwert ist webrole #, wobei # die Anzahl der Webrollen im Dienst angibt.</span><span class="sxs-lookup"><span data-stu-id="5d02c-121">The default is WebRole#, where # indicates the number of web roles in the service.</span></span>

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

### <span data-ttu-id="5d02c-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="5d02c-122">-Profile</span></span>
<span data-ttu-id="5d02c-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="5d02c-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5d02c-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="5d02c-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5d02c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d02c-125">CommonParameters</span></span>
<span data-ttu-id="5d02c-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5d02c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d02c-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d02c-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d02c-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5d02c-128">INPUTS</span></span>

## <span data-ttu-id="5d02c-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5d02c-129">OUTPUTS</span></span>

## <span data-ttu-id="5d02c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="5d02c-130">NOTES</span></span>

## <span data-ttu-id="5d02c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5d02c-131">RELATED LINKS</span></span>

[<span data-ttu-id="5d02c-132">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="5d02c-132">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="5d02c-133">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="5d02c-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


