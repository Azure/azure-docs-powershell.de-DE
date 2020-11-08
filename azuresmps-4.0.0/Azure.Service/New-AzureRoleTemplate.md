---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: E499868E-A745-4CA4-A717-C33C3B94A2C8
online version: ''
schema: 2.0.0
ms.openlocfilehash: b80071bb82ebbb960be5b5b4fcc854dc47c9ed9d
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006198"
---
# <span data-ttu-id="0c8a9-101">New-AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="0c8a9-101">New-AzureRoleTemplate</span></span>

## <span data-ttu-id="0c8a9-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="0c8a9-102">SYNOPSIS</span></span>
<span data-ttu-id="0c8a9-103">Erstellt Web-und worker-Rollenvorlagen.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-103">Creates web and worker role templates.</span></span>

## <span data-ttu-id="0c8a9-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="0c8a9-104">SYNTAX</span></span>

### <span data-ttu-id="0c8a9-105">WebRole</span><span class="sxs-lookup"><span data-stu-id="0c8a9-105">WebRole</span></span>
```
New-AzureRoleTemplate [-Web] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="0c8a9-106">WorkerRole</span><span class="sxs-lookup"><span data-stu-id="0c8a9-106">WorkerRole</span></span>
```
New-AzureRoleTemplate [-Worker] [-Output <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="0c8a9-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c8a9-107">DESCRIPTION</span></span>
<span data-ttu-id="0c8a9-108">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-108">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="0c8a9-109">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="0c8a9-109">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="0c8a9-110">Das Cmdlet **New-AzureRoleTemplate** erstellt Web-und worker-Rollenvorlagen.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-110">The **New-AzureRoleTemplate** cmdlet creates web and worker role templates.</span></span>

## <span data-ttu-id="0c8a9-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="0c8a9-111">EXAMPLES</span></span>

### <span data-ttu-id="0c8a9-112">Beispiel 1: Erstellen einer Webrollen Vorlage</span><span class="sxs-lookup"><span data-stu-id="0c8a9-112">Example 1: Create a web role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Web
```

<span data-ttu-id="0c8a9-113">In diesem Beispiel wird eine neue Webrollen Vorlage in einem Ordner namens "WebRoleTemplate" im aktuellen Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-113">This example creates a new web role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="0c8a9-114">Beispiel 2: Erstellen einer Worker-Rollenvorlage</span><span class="sxs-lookup"><span data-stu-id="0c8a9-114">Example 2: Create a worker role template</span></span>
```
PS C:\> New-AzureRoleTemplate -Worker
```

<span data-ttu-id="0c8a9-115">In diesem Beispiel wird eine neue Worker-Rollenvorlage in einem Ordner namens WebRoleTemplate im aktuellen Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-115">This example creates a new worker role template in a folder named WebRoleTemplate in the current directory.</span></span>

### <span data-ttu-id="0c8a9-116">Beispiel 3: Erstellen einer Rollenvorlage in einem benutzerdefinierten Verzeichnis</span><span class="sxs-lookup"><span data-stu-id="0c8a9-116">Example 3: Create a role template in a custom directory</span></span>
```
PS C:\> New-AzureRoleTemplate -Web -Output C:\MyWebRoleTemplate
```

<span data-ttu-id="0c8a9-117">In diesem Beispiel wird eine neue Webrollen Vorlage im Verzeichnis mit dem Namen MyWebRoleTemplate und nicht im aktuellen Verzeichnis erstellt.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-117">This example creates a new web role template in directory named MyWebRoleTemplate, instead of in the current directory.</span></span>

## <span data-ttu-id="0c8a9-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="0c8a9-118">PARAMETERS</span></span>

### <span data-ttu-id="0c8a9-119">-Output</span><span class="sxs-lookup"><span data-stu-id="0c8a9-119">-Output</span></span>
<span data-ttu-id="0c8a9-120">Gibt den Ausgabepfad der generierten Vorlage an.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-120">Specifies the output path of generated template.</span></span>

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

### <span data-ttu-id="0c8a9-121">-Profil</span><span class="sxs-lookup"><span data-stu-id="0c8a9-121">-Profile</span></span>
<span data-ttu-id="0c8a9-122">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-122">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="0c8a9-123">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-123">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="0c8a9-124">-Web</span><span class="sxs-lookup"><span data-stu-id="0c8a9-124">-Web</span></span>
<span data-ttu-id="0c8a9-125">Gibt an, dass Sie eine Webrollen Vorlage erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-125">Specifies that you want to create a web role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WebRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8a9-126">-Worker</span><span class="sxs-lookup"><span data-stu-id="0c8a9-126">-Worker</span></span>
<span data-ttu-id="0c8a9-127">Gibt an, dass Sie eine Worker-Rollenvorlage erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-127">Specifies that you want to create a worker role template.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: WorkerRole
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0c8a9-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c8a9-128">CommonParameters</span></span>
<span data-ttu-id="0c8a9-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0c8a9-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c8a9-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0c8a9-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c8a9-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="0c8a9-131">INPUTS</span></span>

## <span data-ttu-id="0c8a9-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="0c8a9-132">OUTPUTS</span></span>

## <span data-ttu-id="0c8a9-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="0c8a9-133">NOTES</span></span>

## <span data-ttu-id="0c8a9-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="0c8a9-134">RELATED LINKS</span></span>

[<span data-ttu-id="0c8a9-135">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="0c8a9-135">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="0c8a9-136">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="0c8a9-136">Add-AzureWorkerRole</span></span>](./Add-AzureWorkerRole.md)


