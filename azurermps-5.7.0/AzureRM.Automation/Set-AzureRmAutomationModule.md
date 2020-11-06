---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRmAutomationModule.md
ms.openlocfilehash: 7bec79c2c2c4bdc794b1d3b260cad53d82fa5d4a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93503101"
---
# <span data-ttu-id="a9e82-101">Set-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a9e82-101">Set-AzureRmAutomationModule</span></span>

## <span data-ttu-id="a9e82-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="a9e82-102">SYNOPSIS</span></span>
<span data-ttu-id="a9e82-103">Aktualisiert ein Modul in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a9e82-103">Updates a module in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a9e82-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9e82-104">SYNTAX</span></span>

```
Set-AzureRmAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a9e82-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a9e82-105">DESCRIPTION</span></span>
<span data-ttu-id="a9e82-106">Das Cmdlet " **Satz-AzureRmAutomationModule** " aktualisiert ein Modul in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="a9e82-106">The **Set-AzureRmAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="a9e82-107">Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.</span><span class="sxs-lookup"><span data-stu-id="a9e82-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="a9e82-108">Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält:</span><span class="sxs-lookup"><span data-stu-id="a9e82-108">The file contains a folder that includes a file that is one of the following types:</span></span> 

- <span data-ttu-id="a9e82-109">wps_2 Modul mit der Dateinamenerweiterung psm1 oder dll</span><span class="sxs-lookup"><span data-stu-id="a9e82-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="a9e82-110">wps_2 Modul Manifest mit der Dateinamenerweiterung psd1</span><span class="sxs-lookup"><span data-stu-id="a9e82-110">wps_2 module manifest, which has a .psd1 file name extension</span></span>

<span data-ttu-id="a9e82-111">Der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="a9e82-111">The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>

<span data-ttu-id="a9e82-112">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="a9e82-112">Specify the .zip file as a URL that the Automation service can access.</span></span>

<span data-ttu-id="a9e82-113">Wenn Sie ein wps_2 Modul mithilfe dieses Cmdlets oder des New-AzureRmAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="a9e82-113">If you import a wps_2 module into Automation by using this cmdlet or the New-AzureRmAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="a9e82-114">Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a9e82-114">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="a9e82-115">Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war:</span><span class="sxs-lookup"><span data-stu-id="a9e82-115">To check whether it succeeded, run the following command:</span></span>

<span data-ttu-id="a9e82-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span><span class="sxs-lookup"><span data-stu-id="a9e82-116">`PS C:\\\> $ModuleInstance = Get-AzureRmAutomationModule -Name `ModuleName</span></span>

<span data-ttu-id="a9e82-117">Überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a9e82-117">Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="a9e82-118">Beispiele</span><span class="sxs-lookup"><span data-stu-id="a9e82-118">EXAMPLES</span></span>

### <span data-ttu-id="a9e82-119">Beispiel 1: Aktualisieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="a9e82-119">Example 1: Update a module</span></span>
```
PS C:\>Set-AzureRmAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a9e82-120">Dieser Befehl importiert eine aktualisierte Version eines vorhandenen Moduls mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="a9e82-120">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="a9e82-121">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="a9e82-121">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="a9e82-122">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9e82-122">PARAMETERS</span></span>

### <span data-ttu-id="a9e82-123">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a9e82-123">-AutomationAccountName</span></span>
<span data-ttu-id="a9e82-124">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a9e82-124">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e82-125">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="a9e82-125">-ContentLinkUri</span></span>
<span data-ttu-id="a9e82-126">Gibt die URL der ZIP-Datei an, die die neue Version eines vom Cmdlet importierten Moduls enthält.</span><span class="sxs-lookup"><span data-stu-id="a9e82-126">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e82-127">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="a9e82-127">-ContentLinkVersion</span></span>
<span data-ttu-id="a9e82-128">Gibt die Version des Moduls an, für das dieses Cmdlet die Automatisierung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a9e82-128">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="a9e82-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9e82-129">-DefaultProfile</span></span>
<span data-ttu-id="a9e82-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="a9e82-130">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a9e82-131">-Name</span><span class="sxs-lookup"><span data-stu-id="a9e82-131">-Name</span></span>
<span data-ttu-id="a9e82-132">Gibt den Namen des Moduls an, das dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="a9e82-132">Specifies the name of the module that this cmdlet imports.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e82-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a9e82-133">-ResourceGroupName</span></span>
<span data-ttu-id="a9e82-134">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="a9e82-134">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a9e82-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9e82-135">CommonParameters</span></span>
<span data-ttu-id="a9e82-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a9e82-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9e82-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a9e82-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9e82-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="a9e82-138">INPUTS</span></span>

### <span data-ttu-id="a9e82-139">Keine</span><span class="sxs-lookup"><span data-stu-id="a9e82-139">None</span></span>
<span data-ttu-id="a9e82-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="a9e82-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a9e82-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="a9e82-141">OUTPUTS</span></span>

### <span data-ttu-id="a9e82-142">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="a9e82-142">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="a9e82-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="a9e82-143">NOTES</span></span>

## <span data-ttu-id="a9e82-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="a9e82-144">RELATED LINKS</span></span>

[<span data-ttu-id="a9e82-145">Get-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a9e82-145">Get-AzureRmAutomationModule</span></span>](./Get-AzureRmAutomationModule.md)

[<span data-ttu-id="a9e82-146">Neu – AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a9e82-146">New-AzureRmAutomationModule</span></span>](./New-AzureRmAutomationModule.md)

[<span data-ttu-id="a9e82-147">Remove-AzureRmAutomationModule</span><span class="sxs-lookup"><span data-stu-id="a9e82-147">Remove-AzureRmAutomationModule</span></span>](./Remove-AzureRmAutomationModule.md)


