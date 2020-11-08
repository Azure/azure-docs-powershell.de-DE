---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94177290"
---
# <span data-ttu-id="c74b7-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c74b7-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="c74b7-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c74b7-102">SYNOPSIS</span></span>
<span data-ttu-id="c74b7-103">Aktualisiert ein Modul in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c74b7-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="c74b7-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c74b7-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c74b7-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c74b7-105">DESCRIPTION</span></span>
<span data-ttu-id="c74b7-106">Das Cmdlet " **Satz-AzAutomationModule** " aktualisiert ein Modul in Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="c74b7-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="c74b7-107">Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.</span><span class="sxs-lookup"><span data-stu-id="c74b7-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="c74b7-108">Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält:</span><span class="sxs-lookup"><span data-stu-id="c74b7-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="c74b7-109">wps_2 Modul mit der Dateinamenerweiterung psm1 oder dll</span><span class="sxs-lookup"><span data-stu-id="c74b7-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="c74b7-110">wps_2 Modul Manifest mit einer psd1-Dateinamenerweiterung der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="c74b7-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="c74b7-111">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="c74b7-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="c74b7-112">Wenn Sie ein wps_2 Modul mithilfe dieses Cmdlets oder des New-AzAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="c74b7-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="c74b7-113">Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="c74b7-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="c74b7-114">Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulname überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="c74b7-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="c74b7-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c74b7-115">EXAMPLES</span></span>

### <span data-ttu-id="c74b7-116">Beispiel 1: Aktualisieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="c74b7-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c74b7-117">Dieser Befehl importiert eine aktualisierte Version eines vorhandenen Moduls mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c74b7-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="c74b7-118">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="c74b7-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="c74b7-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="c74b7-119">PARAMETERS</span></span>

### <span data-ttu-id="c74b7-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c74b7-120">-AutomationAccountName</span></span>
<span data-ttu-id="c74b7-121">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c74b7-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c74b7-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="c74b7-122">-ContentLinkUri</span></span>
<span data-ttu-id="c74b7-123">Gibt die URL der ZIP-Datei an, die die neue Version eines vom Cmdlet importierten Moduls enthält.</span><span class="sxs-lookup"><span data-stu-id="c74b7-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: ContentLink

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74b7-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="c74b7-124">-ContentLinkVersion</span></span>
<span data-ttu-id="c74b7-125">Gibt die Version des Moduls an, für das dieses Cmdlet die Automatisierung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c74b7-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c74b7-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c74b7-126">-DefaultProfile</span></span>
<span data-ttu-id="c74b7-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="c74b7-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c74b7-128">-Name</span><span class="sxs-lookup"><span data-stu-id="c74b7-128">-Name</span></span>
<span data-ttu-id="c74b7-129">Gibt den Namen des Moduls an, das dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="c74b7-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="c74b7-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c74b7-130">-ResourceGroupName</span></span>
<span data-ttu-id="c74b7-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="c74b7-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="c74b7-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c74b7-132">CommonParameters</span></span>
<span data-ttu-id="c74b7-133">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c74b7-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c74b7-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c74b7-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c74b7-135">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c74b7-135">INPUTS</span></span>

### <span data-ttu-id="c74b7-136">System. String</span><span class="sxs-lookup"><span data-stu-id="c74b7-136">System.String</span></span>

### <span data-ttu-id="c74b7-137">System. Uri</span><span class="sxs-lookup"><span data-stu-id="c74b7-137">System.Uri</span></span>

## <span data-ttu-id="c74b7-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c74b7-138">OUTPUTS</span></span>

### <span data-ttu-id="c74b7-139">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="c74b7-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="c74b7-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="c74b7-140">NOTES</span></span>

## <span data-ttu-id="c74b7-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c74b7-141">RELATED LINKS</span></span>

[<span data-ttu-id="c74b7-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c74b7-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="c74b7-143">Neu – AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c74b7-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c74b7-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c74b7-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


