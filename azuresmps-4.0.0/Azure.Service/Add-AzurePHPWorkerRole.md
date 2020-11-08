---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: FEFBF1EF-FBCE-45D8-8455-F3F8662F1F36
online version: ''
schema: 2.0.0
ms.openlocfilehash: 4ddf78f30cb6938571fc967d510e4ab99a0cfc80
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006593"
---
# <span data-ttu-id="9dbad-101">Add-AzurePHPWorkerRole</span><span class="sxs-lookup"><span data-stu-id="9dbad-101">Add-AzurePHPWorkerRole</span></span>

## <span data-ttu-id="9dbad-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9dbad-102">SYNOPSIS</span></span>
<span data-ttu-id="9dbad-103">Erstellt die erforderlichen Dateien und die Konfiguration für eine PHP-Anwendung, die in Azure über php.exe gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbad-103">Creates the required files and configuration for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="9dbad-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9dbad-104">SYNTAX</span></span>

```
Add-AzurePHPWorkerRole [-Name <String>] [-Instances <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="9dbad-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9dbad-105">DESCRIPTION</span></span>
<span data-ttu-id="9dbad-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="9dbad-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="9dbad-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="9dbad-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="9dbad-108">Erstellt die erforderlichen Dateien und Konfigurationen, manchmal auch als Gerüst bezeichnet, für eine PHP-Anwendung, die in Azure über php.exe gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbad-108">Creates the required files and configuration, sometimes referred to as scaffolding, for a PHP application that will be hosted in Azure through php.exe.</span></span>

## <span data-ttu-id="9dbad-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9dbad-109">EXAMPLES</span></span>

### <span data-ttu-id="9dbad-110">Beispiel 1: Erstellen einer Worker-Rolle mit einer einzelnen Instanz</span><span class="sxs-lookup"><span data-stu-id="9dbad-110">Example 1: Create a worker role with a single instance</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole
```

<span data-ttu-id="9dbad-111">In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine einzelne Worker-Rolle mit dem Namen "MyWorkerRole" zur aktuellen Anwendung hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9dbad-111">This example adds the required files and configuration for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="9dbad-112">Beispiel 2: Erstellen einer Worker-Rolle mit mehreren Instanzen</span><span class="sxs-lookup"><span data-stu-id="9dbad-112">Example 2: Create a worker role with multiple instances</span></span>
```
PS C:\> Add-AzurePHPWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="9dbad-113">In diesem Beispiel werden die erforderlichen Dateien und die Konfiguration für eine neue Worker-Rolle zur aktuellen Anwendung hinzugefügt, wobei der Name MyWorkerRole mit der Anzahl der Rolleninstanzen von 2 verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9dbad-113">This example adds the required files and configuration for a new worker role to the current application, using the name MyWorkerRole with a role instance count of 2.</span></span>

## <span data-ttu-id="9dbad-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="9dbad-114">PARAMETERS</span></span>

### <span data-ttu-id="9dbad-115">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="9dbad-115">-Instances</span></span>
<span data-ttu-id="9dbad-116">Gibt die Anzahl der Rolleninstanzen für diese Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="9dbad-116">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="9dbad-117">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="9dbad-117">The default is 1.</span></span>

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

### <span data-ttu-id="9dbad-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9dbad-118">-Name</span></span>
<span data-ttu-id="9dbad-119">Gibt den Namen der Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="9dbad-119">Specifies the name of the worker role.</span></span>
<span data-ttu-id="9dbad-120">Der Name bestimmt den Ordnernamen, der die erforderlichen Dateien und die Konfiguration für den in der Worker-Rolle gehosteten php-Dienst enthält.</span><span class="sxs-lookup"><span data-stu-id="9dbad-120">The name determines the folder name that contains the required files and configuration for the PHP service hosted in the worker role.</span></span>
<span data-ttu-id="9dbad-121">Der Standardwert ist WorkerRole1.</span><span class="sxs-lookup"><span data-stu-id="9dbad-121">The default is WorkerRole1.</span></span>

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

### <span data-ttu-id="9dbad-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="9dbad-122">-Profile</span></span>
<span data-ttu-id="9dbad-123">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="9dbad-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="9dbad-124">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="9dbad-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="9dbad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dbad-125">CommonParameters</span></span>
<span data-ttu-id="9dbad-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9dbad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dbad-127">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9dbad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dbad-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9dbad-128">INPUTS</span></span>

## <span data-ttu-id="9dbad-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9dbad-129">OUTPUTS</span></span>

## <span data-ttu-id="9dbad-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="9dbad-130">NOTES</span></span>

## <span data-ttu-id="9dbad-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9dbad-131">RELATED LINKS</span></span>

[<span data-ttu-id="9dbad-132">Neu – AzureServiceProject</span><span class="sxs-lookup"><span data-stu-id="9dbad-132">New-AzureServiceProject</span></span>](./New-AzureServiceProject.md)

[<span data-ttu-id="9dbad-133">Add-AzurePHPWebRole</span><span class="sxs-lookup"><span data-stu-id="9dbad-133">Add-AzurePHPWebRole</span></span>](./Add-AzurePHPWebRole.md)


