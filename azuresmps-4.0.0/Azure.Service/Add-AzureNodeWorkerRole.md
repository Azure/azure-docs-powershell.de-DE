---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 7190C668-6A0C-4E1D-9B5A-0CEEF53E3F85
online version: ''
schema: 2.0.0
ms.openlocfilehash: 93573caf43a6c711e1aa1308c851c82faaef5bcd
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006595"
---
# <span data-ttu-id="3c323-101">Add-AzureNodeWorkerRole</span><span class="sxs-lookup"><span data-stu-id="3c323-101">Add-AzureNodeWorkerRole</span></span>

## <span data-ttu-id="3c323-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3c323-102">SYNOPSIS</span></span>
<span data-ttu-id="3c323-103">Erstellt die erforderlichen Dateien und Ordner für eine Node.js-Anwendung, die in der Cloud gehostet werden soll, über node.exe</span><span class="sxs-lookup"><span data-stu-id="3c323-103">Creates the required files and folders for a Node.js application to be hosted in the cloud via node.exe</span></span>

## <span data-ttu-id="3c323-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3c323-104">SYNTAX</span></span>

```
Add-AzureNodeWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3c323-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3c323-105">DESCRIPTION</span></span>
<span data-ttu-id="3c323-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3c323-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3c323-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3c323-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3c323-108">Das Cmdlet **Add-AzureNodeWorkerRole** erstellt die erforderlichen Dateien und Ordner, manchmal auch als Gerüst bezeichnet, damit eine Node.js Anwendung in der Cloud über node.exe gehostet werden kann.</span><span class="sxs-lookup"><span data-stu-id="3c323-108">The **Add-AzureNodeWorkerRole** cmdlet creates the required files and folders, sometimes referred to as scaffolding, for a Node.js application to be hosted in the cloud via node.exe.</span></span>

## <span data-ttu-id="3c323-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3c323-109">EXAMPLES</span></span>

### <span data-ttu-id="3c323-110">Beispiel 1: worker-Rolle einer einzelnen Instanz</span><span class="sxs-lookup"><span data-stu-id="3c323-110">Example 1: Single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole
```

<span data-ttu-id="3c323-111">In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne Worker-Rolle mit dem Namen **MyWorkerRole** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3c323-111">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application.</span></span>

### <span data-ttu-id="3c323-112">Beispiel 2: worker-Rolle für mehrere Instanzen</span><span class="sxs-lookup"><span data-stu-id="3c323-112">Example 2: Multiple instance worker role</span></span>
```
PS C:\> Add-AzureNodeWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="3c323-113">In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine einzelne Worker-Rolle mit dem Namen **MyWorkerRole** hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="3c323-113">This example adds scaffolding for a single worker role named **MyWorkerRole** to the current application, with a role instance count of 2.</span></span>

## <span data-ttu-id="3c323-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="3c323-114">PARAMETERS</span></span>

### <span data-ttu-id="3c323-115">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="3c323-115">-Instances</span></span>
<span data-ttu-id="3c323-116">Gibt die Anzahl der Rolleninstanzen für diese Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="3c323-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="3c323-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="3c323-117">Default is 1.</span></span>

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

### <span data-ttu-id="3c323-118">-Name</span><span class="sxs-lookup"><span data-stu-id="3c323-118">-Name</span></span>
<span data-ttu-id="3c323-119">Gibt den Namen der Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="3c323-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="3c323-120">Der Wert bestimmt den Ordnernamen, der das Gerüst für den node.js Dienst enthält, der in der Worker-Rolle gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3c323-120">The value determines the folder name that contains the scaffolding for the node.js service hosted in the worker role.</span></span>
<span data-ttu-id="3c323-121">Der Standardwert ist WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="3c323-121">Default is WorkerRole1.</span></span>

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

### <span data-ttu-id="3c323-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="3c323-122">-Profile</span></span>
<span data-ttu-id="3c323-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3c323-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3c323-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3c323-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3c323-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3c323-125">CommonParameters</span></span>
<span data-ttu-id="3c323-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3c323-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3c323-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3c323-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3c323-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3c323-128">INPUTS</span></span>

## <span data-ttu-id="3c323-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3c323-129">OUTPUTS</span></span>

## <span data-ttu-id="3c323-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3c323-130">NOTES</span></span>

## <span data-ttu-id="3c323-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3c323-131">RELATED LINKS</span></span>

[<span data-ttu-id="3c323-132">Add-AzureNodeWebRole</span><span class="sxs-lookup"><span data-stu-id="3c323-132">Add-AzureNodeWebRole</span></span>](./Add-AzureNodeWebRole.md)

[<span data-ttu-id="3c323-133">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="3c323-133">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)


