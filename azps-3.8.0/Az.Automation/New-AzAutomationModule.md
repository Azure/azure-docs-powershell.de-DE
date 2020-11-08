---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 2DC97415-D59A-428E-8FFE-56B17B320DAF
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationModule.md
ms.openlocfilehash: c176c9b8726c4f0edfebcebdc77197f1d555807d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005174"
---
# <span data-ttu-id="e5e7a-101">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e5e7a-101">New-AzAutomationModule</span></span>

## <span data-ttu-id="e5e7a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="e5e7a-102">SYNOPSIS</span></span>
<span data-ttu-id="e5e7a-103">Importiert ein Modul in die Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-103">Imports a module into Automation.</span></span>

## <span data-ttu-id="e5e7a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="e5e7a-104">SYNTAX</span></span>

```
New-AzAutomationModule [-Name] <String> [-ContentLinkUri] <Uri> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e5e7a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5e7a-105">DESCRIPTION</span></span>
<span data-ttu-id="e5e7a-106">Mit dem Cmdlet **New-AzAutomationModule** wird ein Modul in die Azure-Automatisierung importiert.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-106">The **New-AzAutomationModule** cmdlet imports a module into Azure Automation.</span></span>
<span data-ttu-id="e5e7a-107">Dieser Befehl akzeptiert eine komprimierte Datei, die eine ZIP-Dateinamenerweiterung aufweist.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-107">This command accepts a compressed file that has a .zip file name extension.</span></span>
<span data-ttu-id="e5e7a-108">Die Datei enthält einen Ordner, der eine Datei mit einem der folgenden Typen enthält:</span><span class="sxs-lookup"><span data-stu-id="e5e7a-108">The file contains a folder that includes a file that is one of the following types:</span></span> 
- <span data-ttu-id="e5e7a-109">Windows PowerShell-Modul mit einer psm1-oder DLL-Dateinamenerweiterung</span><span class="sxs-lookup"><span data-stu-id="e5e7a-109">Windows PowerShell module, which has a .psm1 or .dll file name extension</span></span> 
- <span data-ttu-id="e5e7a-110">Windows PowerShell-Modul Manifest mit einer psd1-Dateinamenerweiterung der Name der ZIP-Datei, der Name des Ordners und der Name der Datei im Ordner müssen identisch sein.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-110">Windows PowerShell module manifest, which has a .psd1 file name extension The name of the .zip file, the name of the folder, and the name of the file in the folder must be the same.</span></span>
<span data-ttu-id="e5e7a-111">Geben Sie die ZIP-Datei als URL an, auf die der Automatisierungs Dienst zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-111">Specify the .zip file as a URL that the Automation service can access.</span></span>
<span data-ttu-id="e5e7a-112">Wenn Sie ein Windows PowerShell-Modul mithilfe dieses Cmdlets oder des Set-AzAutomationModule-Cmdlets in die Automatisierung importieren, ist der Vorgang asynchron.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-112">If you import a Windows PowerShell module into Automation by using this cmdlet or the Set-AzAutomationModule cmdlet, the operation is asynchronous.</span></span>
<span data-ttu-id="e5e7a-113">Der Befehl beendet, ob der Import erfolgreich ist oder fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-113">The command finishes whether the import succeeds or fails.</span></span>
<span data-ttu-id="e5e7a-114">Führen Sie den folgenden Befehl aus, um zu überprüfen, ob er erfolgreich war: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name ` Modulname überprüfen Sie die **ProvisioningState** -Eigenschaft auf den Wert erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-114">To check whether it succeeded, run the following command: `PS C:\\\> $ModuleInstance = Get-AzAutomationModule -Name `ModuleName Check the **ProvisioningState** property for a value of Succeeded.</span></span>

## <span data-ttu-id="e5e7a-115">Beispiele</span><span class="sxs-lookup"><span data-stu-id="e5e7a-115">EXAMPLES</span></span>

### <span data-ttu-id="e5e7a-116">Beispiel 1: Importieren eines Moduls</span><span class="sxs-lookup"><span data-stu-id="e5e7a-116">Example 1: Import a module</span></span>
```
PS C:\>New-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ContentLink "http://contosostorage.blob.core.windows.net/modules/ContosoModule.zip" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5e7a-117">Dieser Befehl importiert ein Modul mit dem Namen ContosoModule in das Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-117">This command imports a module named ContosoModule into the Automation account named Contoso17.</span></span>
<span data-ttu-id="e5e7a-118">Das Modul wird in einem Azure-BLOB in einem Speicherkonto mit dem Namen contosostorage und einem Container mit dem Namen Module gespeichert.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-118">The module is stored in an Azure blob in a storage account named contosostorage and a container named modules.</span></span>

## <span data-ttu-id="e5e7a-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="e5e7a-119">PARAMETERS</span></span>

### <span data-ttu-id="e5e7a-120">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5e7a-120">-AutomationAccountName</span></span>
<span data-ttu-id="e5e7a-121">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-121">Specifies the name of the Automation account for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="e5e7a-122">-ContentLinkUri</span><span class="sxs-lookup"><span data-stu-id="e5e7a-122">-ContentLinkUri</span></span>
<span data-ttu-id="e5e7a-123">Die URL zu einem Modul-ZIP-Paket</span><span class="sxs-lookup"><span data-stu-id="e5e7a-123">The url to a module zip package</span></span>

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

### <span data-ttu-id="e5e7a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5e7a-124">-DefaultProfile</span></span>
<span data-ttu-id="e5e7a-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="e5e7a-125">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5e7a-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e5e7a-126">-Name</span></span>
<span data-ttu-id="e5e7a-127">Gibt den Namen des Moduls an, das dieses Cmdlet importiert.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-127">Specifies the name of the module that this cmdlet imports.</span></span>

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

### <span data-ttu-id="e5e7a-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5e7a-128">-ResourceGroupName</span></span>
<span data-ttu-id="e5e7a-129">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet ein Modul importiert.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-129">Specifies the name of a resource group for which this cmdlet imports a module.</span></span>

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

### <span data-ttu-id="e5e7a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5e7a-130">CommonParameters</span></span>
<span data-ttu-id="e5e7a-131">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5e7a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5e7a-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5e7a-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5e7a-133">Eingaben</span><span class="sxs-lookup"><span data-stu-id="e5e7a-133">INPUTS</span></span>

### <span data-ttu-id="e5e7a-134">System. String</span><span class="sxs-lookup"><span data-stu-id="e5e7a-134">System.String</span></span>

### <span data-ttu-id="e5e7a-135">System. Uri</span><span class="sxs-lookup"><span data-stu-id="e5e7a-135">System.Uri</span></span>

## <span data-ttu-id="e5e7a-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="e5e7a-136">OUTPUTS</span></span>

### <span data-ttu-id="e5e7a-137">Microsoft. Azure. Commands. Automation. Model. Module</span><span class="sxs-lookup"><span data-stu-id="e5e7a-137">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="e5e7a-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="e5e7a-138">NOTES</span></span>

## <span data-ttu-id="e5e7a-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="e5e7a-139">RELATED LINKS</span></span>

[<span data-ttu-id="e5e7a-140">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e5e7a-140">Get-AzAutomationModule</span></span>](./Get-AzAutomationModule.md)

[<span data-ttu-id="e5e7a-141">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e5e7a-141">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="e5e7a-142">Satz-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="e5e7a-142">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


