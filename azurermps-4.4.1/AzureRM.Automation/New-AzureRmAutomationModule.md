---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: e2de3546f805e006bd7f48e2ee7f95b8f3347544
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93505673"
---
# <span data-ttu-id="e82a8-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e82a8-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="e82a8-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e82a8-102">SYNOPSIS</span></span>
<span data-ttu-id="e82a8-103">Importiert ein Modul in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e82a8-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e82a8-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e82a8-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> -ContentLinkUri <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e82a8-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e82a8-105">DESCRIPTION</span></span>
<span data-ttu-id="e82a8-106">Mit dem Cmdlet **New-AzureRmAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.</span><span class="sxs-lookup"><span data-stu-id="e82a8-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="e82a8-107">Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.</span><span class="sxs-lookup"><span data-stu-id="e82a8-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="e82a8-108">Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält:</span><span class="sxs-lookup"><span data-stu-id="e82a8-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="e82a8-109">wps_2 Modul mit der Dateinamenerweiterung psm1 oder dll</span><span class="sxs-lookup"><span data-stu-id="e82a8-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="e82a8-110">wps_2 Modul Manifest mit der Dateinamenerweiterung psd1</span><span class="sxs-lookup"><span data-stu-id="e82a8-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="e82a8-111">Der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e82a8-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="e82a8-112">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="e82a8-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="e82a8-113">Wenn Sie ein wps_2 Modul mithilfe dieses Cmdlets oder des Set-AzureRmAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="e82a8-113">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="e82a8-114">Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e82a8-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="e82a8-115">Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war:</span><span class="sxs-lookup"><span data-stu-id="e82a8-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="e82a8-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="e82a8-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="e82a8-117">Überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e82a8-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="e82a8-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e82a8-118">EXAMPLES</span></span>

### <span data-ttu-id="e82a8-119">Beispiel 1: Importieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="e82a8-119">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e82a8-120">Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e82a8-120">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="e82a8-121">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e82a8-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="e82a8-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="e82a8-122">PARAMETERS</span></span>

### <span data-ttu-id="e82a8-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e82a8-123">-AutomationAccountName</span></span>
<span data-ttu-id="e82a8-124">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e82a8-124">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a8-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="e82a8-125">-ContentLinkUri</span></span>
<span data-ttu-id="e82a8-126">Die URL zu einem Modul-ZIP-Paket.</span><span class="sxs-lookup"><span data-stu-id="e82a8-126">The url to a module zip package.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a8-127">-Name</span><span class="sxs-lookup"><span data-stu-id="e82a8-127">-Name</span></span>
<span data-ttu-id="e82a8-128">Gibt den Namen des Moduls an, das dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="e82a8-128">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e82a8-129">-ResourceGroupName</span></span>
<span data-ttu-id="e82a8-130">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e82a8-130">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e82a8-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e82a8-131">-DefaultProfile</span></span>
<span data-ttu-id="e82a8-132">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="e82a8-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e82a8-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e82a8-133">CommonParameters</span></span>
<span data-ttu-id="e82a8-134">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e82a8-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e82a8-135">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e82a8-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e82a8-136">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e82a8-136">INPUTS</span></span>

## <span data-ttu-id="e82a8-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e82a8-137">OUTPUTS</span></span>

### <span data-ttu-id="e82a8-138">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="e82a8-138">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="e82a8-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="e82a8-139">NOTES</span></span>

## <span data-ttu-id="e82a8-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e82a8-140">RELATED LINKS</span></span>

[<span data-ttu-id="e82a8-141">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e82a8-141">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="e82a8-142">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e82a8-142">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="e82a8-143">Satz-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e82a8-143">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


