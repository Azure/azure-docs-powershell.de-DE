---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A06D36D7-3F72-4D21-8995-9DBBB9A9B880
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationModule.md
ms.openlocfilehash: 14cd2a45e87fa5042fbf77d4c37d46211f5793a7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100149369"
---
# <span data-ttu-id="6fac3-101">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6fac3-101">Set-AzAutomationModule</span></span>

## <span data-ttu-id="6fac3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6fac3-102">SYNOPSIS</span></span>
<span data-ttu-id="6fac3-103">Aktualisiert ein Modul in der Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="6fac3-103">Updates a module in Automation.</span></span>

## <span data-ttu-id="6fac3-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="6fac3-104">SYNTAX</span></span>

```
Set-AzAutomationModule [-Name] <String> [-ContentLinkUri <Uri>] [-ContentLinkVersion <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6fac3-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="6fac3-105">DESCRIPTION</span></span>
<span data-ttu-id="6fac3-106">Das **Cmdlet "Set-AzAutomationModule"** aktualisiert ein Modul in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="6fac3-106">The **Set-AzAutomationModule** cmdlet updates a module in Azure Automation.</span></span>
<span data-ttu-id="6fac3-107">Dieser Befehl akzeptiert eine komprimierte Datei mit der Dateinamenerweiterung ZIP.</span><span class="sxs-lookup"><span data-stu-id="6fac3-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="6fac3-108">Die Datei enthält einen Ordner, der eine Datei enthält, die einem der folgenden Typen gehört:</span><span class="sxs-lookup"><span data-stu-id="6fac3-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="6fac3-109">wps_2 modul mit der Dateinamenerweiterung PSM1 oder DLL</span><span class="sxs-lookup"><span data-stu-id="6fac3-109">wps_2 module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="6fac3-110">wps_2 Modulmanifest mit der Dateinamenerweiterung PSD1 Der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="6fac3-110">wps_2 module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="6fac3-111">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungsdienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="6fac3-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="6fac3-112">Wenn Sie ein wps_2 mit diesem Cmdlet oder dem New-AzAutomationModule in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="6fac3-112">If you import a wps_2 module into Automation by using this cmdlet or the New-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="6fac3-113">Der Befehl beendet, ob der Importvorgang erfolgreich war oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="6fac3-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="6fac3-114">Um zu überprüfen, ob dies erfolgreich war, führen Sie den folgenden Befehl `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` aus: ModuleName Check **the ProvisioningState** property for a value of Succeeded.</span><span class="sxs-lookup"><span data-stu-id="6fac3-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="6fac3-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="6fac3-115">EXAMPLES</span></span>

### <span data-ttu-id="6fac3-116">Beispiel 1: Aktualisieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="6fac3-116">Example 1: Update a module</span></span>
```
PS C:\>Set-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLinkUri "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ContentLinkVersion "1.1" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6fac3-117">Mit diesem Befehl wird eine aktualisierte Version eines vorhandenen Moduls namens "ContosoModule" in das Automatisierungskonto namens "Contoso17" importiert.</span><span class="sxs-lookup"><span data-stu-id="6fac3-117">This command imports an updated version of an existing module named ContosoModule into the Automation account named Contoso17.</span></span>  <span data-ttu-id="6fac3-118">Das Modul wird in einem Azure-BLOB in einem Speicherkonto namens "contosostorage" und einem Container namens Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="6fac3-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="6fac3-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6fac3-119">PARAMETERS</span></span>

### <span data-ttu-id="6fac3-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6fac3-120">-AutomationAccountName</span></span>
<span data-ttu-id="6fac3-121">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6fac3-121">Specifies the name of the Automation account for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="6fac3-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="6fac3-122">-ContentLinkUri</span></span>
<span data-ttu-id="6fac3-123">Gibt die URL der ZIP-Datei an, die die neue Version eines Moduls enthält, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="6fac3-123">Specifies the URL of the .zip file that contains the new version of a module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="6fac3-124">-ContentLinkVersion</span><span class="sxs-lookup"><span data-stu-id="6fac3-124">-ContentLinkVersion</span></span>
<span data-ttu-id="6fac3-125">Gibt die Version des Moduls an, auf das dieses Cmdlet die Automatisierung aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6fac3-125">Specifies the version of the module to which this cmdlet updates Automation.</span></span>

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

### <span data-ttu-id="6fac3-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fac3-126">-DefaultProfile</span></span>
<span data-ttu-id="6fac3-127">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="6fac3-127">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6fac3-128">-Name</span><span class="sxs-lookup"><span data-stu-id="6fac3-128">-Name</span></span>
<span data-ttu-id="6fac3-129">Gibt den Namen des Moduls an, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="6fac3-129">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="6fac3-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fac3-130">-ResourceGroupName</span></span>
<span data-ttu-id="6fac3-131">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="6fac3-131">Specifies the name of a resource group for which this cmdlet updates a module.</span></span>

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

### <span data-ttu-id="6fac3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fac3-132">CommonParameters</span></span>
<span data-ttu-id="6fac3-133">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fac3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fac3-134">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fac3-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fac3-135">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="6fac3-135">INPUTS</span></span>

### <span data-ttu-id="6fac3-136">System.String</span><span class="sxs-lookup"><span data-stu-id="6fac3-136">System.String</span></span>

### <span data-ttu-id="6fac3-137">System.URI</span><span class="sxs-lookup"><span data-stu-id="6fac3-137">System.Uri</span></span>

## <span data-ttu-id="6fac3-138">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="6fac3-138">OUTPUTS</span></span>

### <span data-ttu-id="6fac3-139">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="6fac3-139">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="6fac3-140">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="6fac3-140">NOTES</span></span>

## <span data-ttu-id="6fac3-141">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="6fac3-141">RELATED LINKS</span></span>

[<span data-ttu-id="6fac3-142">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6fac3-142">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="6fac3-143">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6fac3-143">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="6fac3-144">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="6fac3-144">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)


