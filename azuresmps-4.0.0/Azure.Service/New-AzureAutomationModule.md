---
external help file: Microsoft.Azure.Commands.Automation.dll-Help.xml
ms.assetid: 1F875179-E3CA-4BBB-822A-600777B2D980
online version: ''
schema: 2.0.0
ms.openlocfilehash: c93a09647e22f9d7f1c69cfd6aafe58799217686
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006429"
---
# <span data-ttu-id="1a696-101">New-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a696-101">New-AzureAutomationModule</span></span>

## <span data-ttu-id="1a696-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a696-102">SYNOPSIS</span></span>

<span data-ttu-id="1a696-103">Importiert ein Modul in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="1a696-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="1a696-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a696-104">SYNTAX</span></span>

```
New-AzureAutomationModule -Name <String> -ContentLink <Uri> [-Tags <IDictionary>]
 -AutomationAccountName <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="1a696-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a696-105">DESCRIPTION</span></span>

[!INCLUDE [aa-deprecation](../include/aa-deprecation.md)]

<span data-ttu-id="1a696-106">Mit dem Cmdlet **New-AzureAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.</span><span class="sxs-lookup"><span data-stu-id="1a696-106">The **New-AzureAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="1a696-107">Bei einem Modul handelt es sich um eine komprimierte Datei mit der Erweiterung ZIP, die einen Ordner enthält, der einen der folgenden Dateitypen enthält:</span><span class="sxs-lookup"><span data-stu-id="1a696-107">A module is a compressed file, with a .zip extension, that contains a folder which includes one of the following file types:</span></span>

- <span data-ttu-id="1a696-108">Ein Windows PowerShell-Modul (psm1-Datei).</span><span class="sxs-lookup"><span data-stu-id="1a696-108">A Windows PowerShell module (psm1 file).</span></span> 

- <span data-ttu-id="1a696-109">Ein Windows PowerShell-Modul Manifest (psd1-Datei).</span><span class="sxs-lookup"><span data-stu-id="1a696-109">A Windows PowerShell module manifest (psd1 file).</span></span> 

- <span data-ttu-id="1a696-110">Eine Assembly (DLL-Datei).</span><span class="sxs-lookup"><span data-stu-id="1a696-110">An assembly (dll file).</span></span>

<span data-ttu-id="1a696-111">Die Namen der ZIP-Datei, der Ordner in der ZIP-Datei und die Datei im Ordner (psm1, PSD. 1 oder dll) müssen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="1a696-111">The names of the zip file, the folder in the zip file, and file in the folder (.psm1, psd.1, or .dll) must match.</span></span>

## <span data-ttu-id="1a696-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a696-112">EXAMPLES</span></span>

### <span data-ttu-id="1a696-113">Beispiel 1: Importieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="1a696-113">Example 1: Import a module</span></span>
```
PS C:\> New-AzureAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip"
```

<span data-ttu-id="1a696-114">Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="1a696-114">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="1a696-115">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1a696-115">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="1a696-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a696-116">PARAMETERS</span></span>

### <span data-ttu-id="1a696-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1a696-117">-AutomationAccountName</span></span>
<span data-ttu-id="1a696-118">Gibt den Namen des Automatisierungs Kontos an, in dem das Modul gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a696-118">Specifies the name of the Automation account the module will be stored in.</span></span>

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

### <span data-ttu-id="1a696-119">-ContentLink</span><span class="sxs-lookup"><span data-stu-id="1a696-119">-ContentLink</span></span>
<span data-ttu-id="1a696-120">Öffentliche URL, beispielsweise eine Website oder ein Azure BLOB-Speicher, der den Pfad zur Moduldatei angibt.</span><span class="sxs-lookup"><span data-stu-id="1a696-120">Public URL such as a website or Azure blob storage specifying the path to the module file.</span></span>
<span data-ttu-id="1a696-121">Dieser Speicherort muss öffentlich zugänglich sein.</span><span class="sxs-lookup"><span data-stu-id="1a696-121">This location must be publically accessible.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a696-122">-Name</span><span class="sxs-lookup"><span data-stu-id="1a696-122">-Name</span></span>
<span data-ttu-id="1a696-123">Gibt einen Namen für das Modul an.</span><span class="sxs-lookup"><span data-stu-id="1a696-123">Specifies a name for the module.</span></span>

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

### <span data-ttu-id="1a696-124">-Profil</span><span class="sxs-lookup"><span data-stu-id="1a696-124">-Profile</span></span>
<span data-ttu-id="1a696-125">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="1a696-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="1a696-126">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="1a696-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="1a696-127">-Tags</span><span class="sxs-lookup"><span data-stu-id="1a696-127">-Tags</span></span>
<span data-ttu-id="1a696-128">Gibt einen oder mehrere Tags an, die mit dem Modul verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="1a696-128">Specifies one or more tags related to the module.</span></span>

```yaml
Type: IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1a696-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a696-129">CommonParameters</span></span>
<span data-ttu-id="1a696-130">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a696-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a696-131">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1a696-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a696-132">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a696-132">INPUTS</span></span>

## <span data-ttu-id="1a696-133">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a696-133">OUTPUTS</span></span>

### <span data-ttu-id="1a696-134">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="1a696-134">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="1a696-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a696-135">NOTES</span></span>

## <span data-ttu-id="1a696-136">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a696-136">RELATED LINKS</span></span>

[<span data-ttu-id="1a696-137">Get-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a696-137">Get-AzureAutomationModule</span></span>](./Get-AzureAutomationModule.md)

[<span data-ttu-id="1a696-138">Remove-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a696-138">Remove-AzureAutomationModule</span></span>](./Remove-AzureAutomationModule.md)

[<span data-ttu-id="1a696-139">Satz-AzureAutomationModule</span><span class="sxs-lookup"><span data-stu-id="1a696-139">Set-AzureAutomationModule</span></span>](./Set-AzureAutomationModule.md)


