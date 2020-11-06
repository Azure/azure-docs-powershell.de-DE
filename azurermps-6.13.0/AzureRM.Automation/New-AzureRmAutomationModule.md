---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationModule.md
ms.openlocfilehash: 0ddfbd8aceeb26a4f40fcf104919fa9b67b39aa3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476273"
---
# <span data-ttu-id="64643-101">New-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="64643-101">New-AzureRmAutomationModule</span></span>

## <span data-ttu-id="64643-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="64643-102">SYNOPSIS</span></span>
<span data-ttu-id="64643-103">Importiert ein Modul in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="64643-103">Imports a module into Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="64643-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="64643-104">SYNTAX</span></span>

```
New-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="64643-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="64643-105">DESCRIPTION</span></span>
<span data-ttu-id="64643-106">Mit dem Cmdlet **New-AzureRmAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.</span><span class="sxs-lookup"><span data-stu-id="64643-106">The **New-AzureRmAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="64643-107">Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.</span><span class="sxs-lookup"><span data-stu-id="64643-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="64643-108">Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält:</span><span class="sxs-lookup"><span data-stu-id="64643-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="64643-109">wps_2 Modul mit der Dateinamenerweiterung psm1 oder dll</span><span class="sxs-lookup"><span data-stu-id="64643-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="64643-110">wps_2 Modul Manifest mit einer psd1-Dateinamenerweiterung der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="64643-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="64643-111">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="64643-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="64643-112">Wenn Sie ein wps_2 Modul mithilfe dieses Cmdlets oder des Set-AzureRmAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="64643-112">If you import a wps_2 module into Automation by using this cmdlet or the Set-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="64643-113">Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="64643-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="64643-114">Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name ` Modulname überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="64643-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="64643-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="64643-115">EXAMPLES</span></span>

### <span data-ttu-id="64643-116">Beispiel 1: Importieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="64643-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="64643-117">Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="64643-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="64643-118">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="64643-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="64643-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="64643-119">PARAMETERS</span></span>

### <span data-ttu-id="64643-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="64643-120">-AutomationAccountName</span></span>
<span data-ttu-id="64643-121">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="64643-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="64643-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="64643-122">-ContentLinkUri</span></span>
<span data-ttu-id="64643-123">Die URL zu einem Modul-ZIP-Paket</span><span class="sxs-lookup"><span data-stu-id="64643-123">The url to a module zip package</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="64643-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="64643-124">-DefaultProfile</span></span>
<span data-ttu-id="64643-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="64643-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="64643-126">-Name</span><span class="sxs-lookup"><span data-stu-id="64643-126">-Name</span></span>
<span data-ttu-id="64643-127">Gibt den Namen des Moduls an, das dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="64643-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="64643-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="64643-128">-ResourceGroupName</span></span>
<span data-ttu-id="64643-129">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="64643-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="64643-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="64643-130">CommonParameters</span></span>
<span data-ttu-id="64643-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="64643-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="64643-132">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="64643-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="64643-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="64643-133">INPUTS</span></span>

### <span data-ttu-id="64643-134">System. String</span><span class="sxs-lookup"><span data-stu-id="64643-134">System.String</span></span>

### <span data-ttu-id="64643-135">System. Uri</span><span class="sxs-lookup"><span data-stu-id="64643-135">System.Uri</span></span>

## <span data-ttu-id="64643-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="64643-136">OUTPUTS</span></span>

### <span data-ttu-id="64643-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="64643-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="64643-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="64643-138">NOTES</span></span>

## <span data-ttu-id="64643-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="64643-139">RELATED LINKS</span></span>

[<span data-ttu-id="64643-140">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="64643-140">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="64643-141">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="64643-141">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)

[<span data-ttu-id="64643-142">Satz-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="64643-142">Set-AzureRmAutomationModule</span></span>](./Set-AzureRmAutomationModule.md)


