---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 2261AD64-196A-402E-9703-EFB3A6D75FA7
online version: ''
schema: 2.0.0
ms.openlocfilehash: d83ed3e336ca72e38fc16c27ec696eea0f84f746
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006424"
---
# <span data-ttu-id="7e0a1-101">New-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7e0a1-101">New-AzureServiceProject</span></span>

## <span data-ttu-id="7e0a1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7e0a1-102">SYNOPSIS</span></span>
<span data-ttu-id="7e0a1-103">Erstellt die erforderlichen Dateien und die Konfiguration für einen neuen Dienst.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-103">Creates the required files and configuration for a new service.</span></span>

## <span data-ttu-id="7e0a1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7e0a1-104">SYNTAX</span></span>

```
New-AzureServiceProject -ServiceName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7e0a1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7e0a1-105">DESCRIPTION</span></span>
<span data-ttu-id="7e0a1-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="7e0a1-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="7e0a1-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="7e0a1-108">Das Cmdlet **New-AzureServiceProject** erstellt die erforderlichen Dateien und die Konfiguration für einen neuen Azure-Dienst im aktuellen Verzeichnis.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-108">The **New-AzureServiceProject** cmdlet creates the required files and configuration for a new Azure service in the current directory.</span></span>

## <span data-ttu-id="7e0a1-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7e0a1-109">EXAMPLES</span></span>

### <span data-ttu-id="7e0a1-110">Beispiel 1: Erstellen eines Gerüsts für einen Dienst</span><span class="sxs-lookup"><span data-stu-id="7e0a1-110">Example 1: Create scaffolding for a service</span></span>
```
PS C:\> New-AzureServiceProject MyService1
```

<span data-ttu-id="7e0a1-111">In diesem Beispiel wird ein Gerüst für einen neuen Azure-Dienst mit dem Namen MyService1 im aktuellen Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-111">This example creates scaffolding for a new Azure service named MyService1 in the current directory.</span></span>

## <span data-ttu-id="7e0a1-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="7e0a1-112">PARAMETERS</span></span>

### <span data-ttu-id="7e0a1-113">-Profil</span><span class="sxs-lookup"><span data-stu-id="7e0a1-113">-Profile</span></span>
<span data-ttu-id="7e0a1-114">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-114">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="7e0a1-115">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-115">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="7e0a1-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="7e0a1-116">-ServiceName</span></span>
<span data-ttu-id="7e0a1-117">Gibt den Namen des Diensts an.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-117">Specifies the name of the service.</span></span>
<span data-ttu-id="7e0a1-118">Sie bestimmt den ersten Abschnitt des Hostnamens für Ihren Dienst (beispielsweise Name.cloudapp.net) und das Verzeichnis, in dem Ihr Dienst enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-118">It determines the first section of the hostname for your service (for example, name.cloudapp.net), and the directory that will contain your service.</span></span>
<span data-ttu-id="7e0a1-119">Der Name darf nur Buchstaben, Ziffern und das Bindestrichzeichen (-) enthalten.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-119">The name can contain only letters, digits, and the dash character (-).</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7e0a1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e0a1-120">CommonParameters</span></span>
<span data-ttu-id="7e0a1-121">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7e0a1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e0a1-122">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7e0a1-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e0a1-123">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7e0a1-123">INPUTS</span></span>

## <span data-ttu-id="7e0a1-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7e0a1-124">OUTPUTS</span></span>

## <span data-ttu-id="7e0a1-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="7e0a1-125">NOTES</span></span>

## <span data-ttu-id="7e0a1-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7e0a1-126">RELATED LINKS</span></span>

[<span data-ttu-id="7e0a1-127">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="7e0a1-127">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="7e0a1-128">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="7e0a1-128">Add-AzureNodeWorkerRole</span></span>](./Add-AzureNodeWorkerRole.md)

[<span data-ttu-id="7e0a1-129">Publish-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7e0a1-129">Publish-AzureServiceProject</span></span>](./Publish-AzureServiceProject.md)

[<span data-ttu-id="7e0a1-130">Satz-AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="7e0a1-130">Set-AzureServiceProject</span></span>](./Set-AzureServiceProject.md)

[<span data-ttu-id="7e0a1-131">Satz-AzureServiceProjectRole</span><span class="sxs-lookup"><span data-stu-id="7e0a1-131">Set-AzureServiceProjectRole</span></span>](./Set-AzureServiceProjectRole.md)


