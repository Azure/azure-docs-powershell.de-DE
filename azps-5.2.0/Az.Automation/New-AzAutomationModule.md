---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373552"
---
# <span data-ttu-id="e8352-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e8352-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="e8352-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8352-102">SYNOPSIS</span></span>
<span data-ttu-id="e8352-103">Importiert ein Modul in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e8352-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="e8352-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="e8352-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e8352-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="e8352-105">DESCRIPTION</span></span>
<span data-ttu-id="e8352-106">Das **Cmdlet "New-AzAutomationModule"** importiert ein Modul in die Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e8352-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="e8352-107">Dieser Befehl akzeptiert eine komprimierte Datei mit der Dateinamenerweiterung ZIP.</span><span class="sxs-lookup"><span data-stu-id="e8352-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="e8352-108">Die Datei enthält einen Ordner, der eine Datei enthält, die einem der folgenden Typen gehört:</span><span class="sxs-lookup"><span data-stu-id="e8352-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="e8352-109">Windows PowerShell modul mit der Dateinamenerweiterung PSM1 oder DLL</span><span class="sxs-lookup"><span data-stu-id="e8352-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="e8352-110">Windows PowerShell Modulmanifest mit der Dateinamenerweiterung PSD1 Der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e8352-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="e8352-111">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungsdienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="e8352-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="e8352-112">Wenn Sie ein Windows PowerShell mit diesem Cmdlet oder dem cmdlet Set-AzAutomationModule in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="e8352-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="e8352-113">Der Befehl beendet, ob der Importvorgang erfolgreich war oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e8352-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="e8352-114">Um zu überprüfen, ob dies erfolgreich war, führen Sie den folgenden Befehl `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` aus: ModuleName Check **the ProvisioningState** property for a value of Succeeded.</span><span class="sxs-lookup"><span data-stu-id="e8352-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="e8352-115">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="e8352-115">EXAMPLES</span></span>

### <span data-ttu-id="e8352-116">Beispiel 1: Importieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="e8352-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e8352-117">Mit diesem Befehl wird ein Modul namens "ContosoModule" in das Automatisierungskonto namens "Contoso17" importiert.</span><span class="sxs-lookup"><span data-stu-id="e8352-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="e8352-118">Das Modul wird in einem Azure-BLOB in einem Speicherkonto namens "contosostorage" und einem Container namens Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e8352-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="e8352-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8352-119">PARAMETERS</span></span>

### <span data-ttu-id="e8352-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e8352-120">-AutomationAccountName</span></span>
<span data-ttu-id="e8352-121">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e8352-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="e8352-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="e8352-122">-ContentLinkUri</span></span>
<span data-ttu-id="e8352-123">Die URL eines Modul-ZIP-Pakets</span><span class="sxs-lookup"><span data-stu-id="e8352-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="e8352-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8352-124">-DefaultProfile</span></span>
<span data-ttu-id="e8352-125">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="e8352-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8352-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e8352-126">-Name</span></span>
<span data-ttu-id="e8352-127">Gibt den Namen des Moduls an, das von diesem Cmdlet importiert wird.</span><span class="sxs-lookup"><span data-stu-id="e8352-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="e8352-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8352-128">-ResourceGroupName</span></span>
<span data-ttu-id="e8352-129">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e8352-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="e8352-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8352-130">CommonParameters</span></span>
<span data-ttu-id="e8352-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8352-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8352-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8352-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8352-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="e8352-133">INPUTS</span></span>

### <span data-ttu-id="e8352-134">System.String</span><span class="sxs-lookup"><span data-stu-id="e8352-134">System.String</span></span>

### <span data-ttu-id="e8352-135">System.URI</span><span class="sxs-lookup"><span data-stu-id="e8352-135">System.Uri</span></span>

## <span data-ttu-id="e8352-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="e8352-136">OUTPUTS</span></span>

### <span data-ttu-id="e8352-137">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="e8352-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="e8352-138">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="e8352-138">NOTES</span></span>

## <span data-ttu-id="e8352-139">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="e8352-139">RELATED LINKS</span></span>

[<span data-ttu-id="e8352-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e8352-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="e8352-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e8352-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="e8352-142">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e8352-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


