---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: F9A06B8B-55DB-48A5-B246-53347E759E64
online version: ''
schema: 2.0.0
ms.openlocfilehash: 050c05f2cdad546388744bcebca4f28a12a03038
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006596"
---
# <span data-ttu-id="ee8c7-101">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="ee8c7-101">Add-AzurePHPWebRole</span></span>

## <span data-ttu-id="ee8c7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ee8c7-102">SYNOPSIS</span></span>
<span data-ttu-id="ee8c7-103">Erstellt die erforderlichen Dateien und die Konfiguration für eine PHP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-103">Creates the required files and configuration for a PHP application.</span></span>

## <span data-ttu-id="ee8c7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ee8c7-104">SYNTAX</span></span>

```
Add-AzurePHPWebRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="ee8c7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ee8c7-105">DESCRIPTION</span></span>
<span data-ttu-id="ee8c7-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="ee8c7-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="ee8c7-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="ee8c7-108">Mit dem Cmdlet **Add-AzurePHPWebRole** werden die Dateien und die Konfiguration, manchmal auch als Gerüst bezeichnet, für eine PHP-Anwendung erstellt, die in Azure über IIS gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-108">The **Add-AzurePHPWebRole** cmdlet creates the files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through IIS.</span></span>

## <span data-ttu-id="ee8c7-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ee8c7-109">EXAMPLES</span></span>

### <span data-ttu-id="ee8c7-110">Beispiel 1: Hinzufügen einer webrolle mit Standardwerten</span><span class="sxs-lookup"><span data-stu-id="ee8c7-110">Example 1: Add a web role using default values</span></span>
```
PS C:\> Add-AzurePHPWebRole
```

<span data-ttu-id="ee8c7-111">In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für die neue webrolle unter Verwendung der Standardwerte für einen Dienst mit dem Namen "WebRole1" mit einer 1-Instanz hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-111">This example adds the required files and configuration for new web role using the default values of a service named "WebRole1" with 1 instance.</span></span>

### <span data-ttu-id="ee8c7-112">Beispiel 2: Hinzufügen einer webrolle mit mehreren Instanzen</span><span class="sxs-lookup"><span data-stu-id="ee8c7-112">Example 2: Add a web role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWebRole MyWebRole -I 2
```

<span data-ttu-id="ee8c7-113">In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine neue webrolle zur aktuellen Anwendung hinzugefügt, wobei der Name "MyWebRole" und die Anzahl der Rolleninstanzen von 2 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-113">This example adds the required files and configuration for a new web role to the current application, using the name "MyWebRole" and a role instance count of 2.</span></span>

## <span data-ttu-id="ee8c7-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="ee8c7-114">PARAMETERS</span></span>

### <span data-ttu-id="ee8c7-115">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="ee8c7-115">-Instances</span></span>
<span data-ttu-id="ee8c7-116">Gibt die Anzahl der Rolleninstanzen für diese webrolle an.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-116">Specifies the number of role instances for this web role.</span></span>
<span data-ttu-id="ee8c7-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-117">The default is 1.</span></span>

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

### <span data-ttu-id="ee8c7-118">-Name</span><span class="sxs-lookup"><span data-stu-id="ee8c7-118">-Name</span></span>
<span data-ttu-id="ee8c7-119">Gibt den Namen der webrolle an.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-119">Specifies the name of the web role.</span></span>
<span data-ttu-id="ee8c7-120">Der Name bestimmt den Namen des Verzeichnisses, in dem die erforderlichen Dateien und die Konfiguration für die PHP-Anwendung enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-120">The name determines the name of the directory that contains the required files and configuration for the PHP application.</span></span>
<span data-ttu-id="ee8c7-121">Der Standardwert ist webrole #, wobei # die Anzahl der Webrollen im Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-121">The default is WebRole#, where # is the number of web roles in the service.</span></span>

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

### <span data-ttu-id="ee8c7-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="ee8c7-122">-Profile</span></span>
<span data-ttu-id="ee8c7-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="ee8c7-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="ee8c7-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee8c7-125">CommonParameters</span></span>
<span data-ttu-id="ee8c7-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ee8c7-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee8c7-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ee8c7-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee8c7-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ee8c7-128">INPUTS</span></span>

## <span data-ttu-id="ee8c7-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ee8c7-129">OUTPUTS</span></span>

## <span data-ttu-id="ee8c7-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="ee8c7-130">NOTES</span></span>

## <span data-ttu-id="ee8c7-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ee8c7-131">RELATED LINKS</span></span>

[<span data-ttu-id="ee8c7-132">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="ee8c7-132">Add-AzurePHPWorkerRole</span></span>](./Add-AzurePHPWorkerRole.md)

[<span data-ttu-id="ee8c7-133">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="ee8c7-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


