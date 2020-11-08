---
external help file: Microsoft.WindowsAzure.Commands.dll-Help.xml
ms.assetid: 8632A865-D4CC-4AE5-8307-055CDD776D26
online version: ''
schema: 2.0.0
ms.openlocfilehash: a2b79ee50bb5097896c2a120a9b7316adb2146b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94005916"
---
# <span data-ttu-id="3f37a-101">Add-AzureWorkerRole</span><span class="sxs-lookup"><span data-stu-id="3f37a-101">Add-AzureWorkerRole</span></span>

## <span data-ttu-id="3f37a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3f37a-102">SYNOPSIS</span></span>
<span data-ttu-id="3f37a-103">Erstellt erforderliche Dateien und Konfiguration für eine benutzerdefinierte Worker-Rolle.</span><span class="sxs-lookup"><span data-stu-id="3f37a-103">Creates required files and configuration for a custom worker role.</span></span>

## <span data-ttu-id="3f37a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3f37a-104">SYNTAX</span></span>

```
Add-AzureWorkerRole [-TemplateFolder <String>] [-Name <String>] [-Instances <Int32>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="3f37a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3f37a-105">DESCRIPTION</span></span>
<span data-ttu-id="3f37a-106">In diesem Thema wird das Cmdlet in der 0.8.10-Version des Microsoft Azure PowerShell-Moduls beschrieben.</span><span class="sxs-lookup"><span data-stu-id="3f37a-106">This topic describes the cmdlet in the 0.8.10 version of the Microsoft Azure PowerShell module.</span></span>
<span data-ttu-id="3f37a-107">Wenn Sie die Version des verwendeten Moduls abrufen möchten, geben Sie in der Azure PowerShell-Konsole `(Get-Module -Name Azure).Version` .</span><span class="sxs-lookup"><span data-stu-id="3f37a-107">To get the version of the module you're using, in the Azure PowerShell console, type `(Get-Module -Name Azure).Version`.</span></span>

<span data-ttu-id="3f37a-108">Das Cmdlet **Add-AzureWorkerRole** erstellt erforderliche Dateien und Konfigurationen, manchmal auch als Gerüst bezeichnet, für eine benutzerdefinierte Worker-Rolle.</span><span class="sxs-lookup"><span data-stu-id="3f37a-108">The **Add-AzureWorkerRole** cmdlet creates required files and configuration, sometimes referred to as scaffolding, for a custom worker role.</span></span>

## <span data-ttu-id="3f37a-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3f37a-109">EXAMPLES</span></span>

### <span data-ttu-id="3f37a-110">Beispiel 1: Erstellen einer einzelnen Instanzen-Worker-Rolle</span><span class="sxs-lookup"><span data-stu-id="3f37a-110">Example 1: Create a single instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole -Name MyWorkerRole
```

<span data-ttu-id="3f37a-111">In diesem Beispiel wird der aktuellen Anwendung Gerüstbau für eine einzelne Worker-Rolle mit dem Namen MyWorkerRole hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="3f37a-111">This example adds scaffolding for a single worker role named MyWorkerRole to the current application.</span></span>

### <span data-ttu-id="3f37a-112">Beispiel 2: Erstellen einer Worker-Rolle für mehrere Instanzen</span><span class="sxs-lookup"><span data-stu-id="3f37a-112">Example 2: Create a multiple instance worker role</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -I 2
```

<span data-ttu-id="3f37a-113">In diesem Beispiel wird der aktuellen Anwendung ein Gerüst für eine neue Worker-Rolle mit dem Namen MyWorkerRole hinzugefügt, wobei die Anzahl der Rolleninstanzen 2 beträgt.</span><span class="sxs-lookup"><span data-stu-id="3f37a-113">This example adds scaffolding for a new worker role named MyWorkerRole to the current application, with a role instance count of 2.</span></span>

### <span data-ttu-id="3f37a-114">Beispiel 3: Erstellen einer Worker-Rolle mit benutzerdefiniertem Gerüst</span><span class="sxs-lookup"><span data-stu-id="3f37a-114">Example 3: Create worker role with custom scaffolding</span></span>
```
PS C:\> Add-AzureWorkerRole MyWorkerRole -TemplateFoldr .\MyWorkerRoleTemplate
```

<span data-ttu-id="3f37a-115">In diesem Beispiel wird eine Worker-Rolle mit benutzerdefiniertem Gerüst erstellt.</span><span class="sxs-lookup"><span data-stu-id="3f37a-115">This example creates a worker role with custom scaffolding.</span></span>

## <span data-ttu-id="3f37a-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3f37a-116">PARAMETERS</span></span>

### <span data-ttu-id="3f37a-117">-Instanzen</span><span class="sxs-lookup"><span data-stu-id="3f37a-117">-Instances</span></span>
<span data-ttu-id="3f37a-118">Gibt die Anzahl der Rolleninstanzen für diese Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="3f37a-118">Specifies the number of role instances for this worker role.</span></span>
<span data-ttu-id="3f37a-119">Der Standardwert ist 1.</span><span class="sxs-lookup"><span data-stu-id="3f37a-119">The default is 1.</span></span>

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

### <span data-ttu-id="3f37a-120">-Name</span><span class="sxs-lookup"><span data-stu-id="3f37a-120">-Name</span></span>
<span data-ttu-id="3f37a-121">Gibt den Namen der Worker-Rolle an.</span><span class="sxs-lookup"><span data-stu-id="3f37a-121">Specifies the name of the worker role.</span></span>
<span data-ttu-id="3f37a-122">Dieser Wert bestimmt den Ordnernamen, der das Gerüst für die benutzerdefinierte Anwendung enthält, die in der Worker-Rolle gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3f37a-122">This value determines the folder name that contains the scaffolding for the custom application that will be hosted in the worker role.</span></span>
<span data-ttu-id="3f37a-123">Der Standardwert ist "WorkerRolenumber", wobei "Zahl" die Anzahl der Worker-Rollen im Dienst ist.</span><span class="sxs-lookup"><span data-stu-id="3f37a-123">The default is WorkerRolenumber, where number is the number of worker roles in the service.</span></span>

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

### <span data-ttu-id="3f37a-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="3f37a-124">-Profile</span></span>
<span data-ttu-id="3f37a-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3f37a-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3f37a-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3f37a-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3f37a-127">-TemplateFolder</span><span class="sxs-lookup"><span data-stu-id="3f37a-127">-TemplateFolder</span></span>
<span data-ttu-id="3f37a-128">Gibt den Gerüst Vorlagenordner an, der zum Erstellen der Worker-Rolle verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="3f37a-128">Specifies the scaffolding template folder to be used to create the worker role.</span></span>

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

### <span data-ttu-id="3f37a-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3f37a-129">CommonParameters</span></span>
<span data-ttu-id="3f37a-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3f37a-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3f37a-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3f37a-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3f37a-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3f37a-132">INPUTS</span></span>

## <span data-ttu-id="3f37a-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3f37a-133">OUTPUTS</span></span>

## <span data-ttu-id="3f37a-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="3f37a-134">NOTES</span></span>

## <span data-ttu-id="3f37a-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3f37a-135">RELATED LINKS</span></span>

[<span data-ttu-id="3f37a-136">Add-AzureWebRole</span><span class="sxs-lookup"><span data-stu-id="3f37a-136">Add-AzureWebRole</span></span>](./Add-AzureWebRole.md)

[<span data-ttu-id="3f37a-137">Neu – AzureRoleTemplate</span><span class="sxs-lookup"><span data-stu-id="3f37a-137">New-AzureRoleTemplate</span></span>](./New-AzureRoleTemplate.md)


