---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: A73B388A-E859-40D3-BA63-0E231CF1E81D
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationmodule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationModule.md
ms.openlocfilehash: 978e1bf2e826e576745748c43249bf8257f129cc
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949768"
---
# <span data-ttu-id="c7e0b-101">Get-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c7e0b-101">Get-AzAutomationModule</span></span>

## <span data-ttu-id="c7e0b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c7e0b-102">SYNOPSIS</span></span>
<span data-ttu-id="c7e0b-103">Ruft Metadaten für Module aus der Automatisierung ab.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-103">Gets metadata for modules from Automation.</span></span>

## <span data-ttu-id="c7e0b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c7e0b-104">SYNTAX</span></span>

### <span data-ttu-id="c7e0b-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="c7e0b-105">ByAll (Default)</span></span>
```
Get-AzAutomationModule [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c7e0b-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c7e0b-106">ByName</span></span>
```
Get-AzAutomationModule [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7e0b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c7e0b-107">DESCRIPTION</span></span>
<span data-ttu-id="c7e0b-108">Das **Get-AzAutomationModule-Cmdlet** ruft Metadaten für Module aus Azure Automation ab.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-108">The **Get-AzAutomationModule** cmdlet gets metadata for modules from Azure Automation.</span></span>

## <span data-ttu-id="c7e0b-109">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c7e0b-109">EXAMPLES</span></span>

### <span data-ttu-id="c7e0b-110">Beispiel 1: Alle Module erhalten</span><span class="sxs-lookup"><span data-stu-id="c7e0b-110">Example 1: Get all modules</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c7e0b-111">Dieser Befehl ruft alle Module im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-111">This command gets all modules in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c7e0b-112">Beispiel 2: Erhalten eines Moduls</span><span class="sxs-lookup"><span data-stu-id="c7e0b-112">Example 2: Get a module</span></span>
```
PS C:\>Get-AzAutomationModule -AutomationAccountName "Contoso17" -Name "ContosoModule" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="c7e0b-113">Dieser Befehl ruft ein Modul namens ContosoModule im Automatisierungskonto namens Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-113">This command gets a module named ContosoModule in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c7e0b-114">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="c7e0b-114">PARAMETERS</span></span>

### <span data-ttu-id="c7e0b-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c7e0b-115">-AutomationAccountName</span></span>
<span data-ttu-id="c7e0b-116">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet Modulmetadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-116">Specifies the name of the Automation account for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="c7e0b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7e0b-117">-DefaultProfile</span></span>
<span data-ttu-id="c7e0b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c7e0b-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c7e0b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="c7e0b-119">-Name</span></span>
<span data-ttu-id="c7e0b-120">Gibt den Namen des Moduls an, für das dieses Cmdlet Metadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-120">Specifies the name of the module for which this cmdlet gets metadata.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c7e0b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c7e0b-121">-ResourceGroupName</span></span>
<span data-ttu-id="c7e0b-122">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet Modulmetadaten erhält.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-122">Specifies the name of a resource group for which this cmdlet gets module metadata.</span></span>

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

### <span data-ttu-id="c7e0b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7e0b-123">CommonParameters</span></span>
<span data-ttu-id="c7e0b-124">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7e0b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7e0b-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7e0b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7e0b-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c7e0b-126">INPUTS</span></span>

### <span data-ttu-id="c7e0b-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c7e0b-127">System.String</span></span>

## <span data-ttu-id="c7e0b-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c7e0b-128">OUTPUTS</span></span>

### <span data-ttu-id="c7e0b-129">Microsoft.Azure.Commands.Automation.Model.Module</span><span class="sxs-lookup"><span data-stu-id="c7e0b-129">Microsoft.Azure.Commands.Automation.Model.Module</span></span>

## <span data-ttu-id="c7e0b-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="c7e0b-130">NOTES</span></span>

## <span data-ttu-id="c7e0b-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="c7e0b-131">RELATED LINKS</span></span>

[<span data-ttu-id="c7e0b-132">New-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c7e0b-132">New-AzAutomationModule</span></span>](./New-AzAutomationModule.md)

[<span data-ttu-id="c7e0b-133">Remove-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c7e0b-133">Remove-AzAutomationModule</span></span>](./Remove-AzAutomationModule.md)

[<span data-ttu-id="c7e0b-134">Set-AzAutomationModule</span><span class="sxs-lookup"><span data-stu-id="c7e0b-134">Set-AzAutomationModule</span></span>](./Set-AzAutomationModule.md)


