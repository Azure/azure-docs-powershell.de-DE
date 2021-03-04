---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 8FB78A4A-8392-44EE-A907-10FDF756071B
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationVariable.md
ms.openlocfilehash: c30e78b21c8f0dbc59e12c0fbecad14cfc93781a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101949680"
---
# <span data-ttu-id="5e360-101">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5e360-101">Get-AzAutomationVariable</span></span>

## <span data-ttu-id="5e360-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e360-102">SYNOPSIS</span></span>
<span data-ttu-id="5e360-103">Ruft eine Automatisierungsvariable ab.</span><span class="sxs-lookup"><span data-stu-id="5e360-103">Gets an Automation variable.</span></span>

## <span data-ttu-id="5e360-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5e360-104">SYNTAX</span></span>

### <span data-ttu-id="5e360-105">ByAll (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e360-105">ByAll (Default)</span></span>
```
Get-AzAutomationVariable [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5e360-106">ByName</span><span class="sxs-lookup"><span data-stu-id="5e360-106">ByName</span></span>
```
Get-AzAutomationVariable [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5e360-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5e360-107">DESCRIPTION</span></span>
<span data-ttu-id="5e360-108">Das **Get-AzAutomationVariable-Cmdlet** ruft mindestens eine Azure-Automatisierungsvariable ab.</span><span class="sxs-lookup"><span data-stu-id="5e360-108">The **Get-AzAutomationVariable** cmdlet gets one or more Azure Automation variables.</span></span>
<span data-ttu-id="5e360-109">Um eine bestimmte Variable zu erhalten, geben Sie deren Namen an.</span><span class="sxs-lookup"><span data-stu-id="5e360-109">To get a specific variable, specify its name.</span></span>

## <span data-ttu-id="5e360-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5e360-110">EXAMPLES</span></span>

### <span data-ttu-id="5e360-111">Beispiel 1: Erhalten einer Variablen</span><span class="sxs-lookup"><span data-stu-id="5e360-111">Example 1: Get a variable</span></span>
```
PS C:\>$Variable = Get-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "Variable06" -ResourceGroupName "ResourceGroup01"
PS C:\> $Value = $Variable.value
```

<span data-ttu-id="5e360-112">Der erste Befehl ruft eine Automatisierungsvariable namens Variable06 im Konto mit dem Namen Contoso17 ab.</span><span class="sxs-lookup"><span data-stu-id="5e360-112">The first command gets an Automation variable named Variable06 in the account named Contoso17.</span></span>
<span data-ttu-id="5e360-113">Der Befehl speichert dieses Objekt in der $Variable-Variable.</span><span class="sxs-lookup"><span data-stu-id="5e360-113">The command stores that object in the $Variable variable.</span></span>
<span data-ttu-id="5e360-114">Der zweite Befehl verwendet die Standardpunkt-Notation, um auf die **Werteigenschaft** $Variable.</span><span class="sxs-lookup"><span data-stu-id="5e360-114">The second command uses standard dot notation to refer to the **value** property of $Variable.</span></span>
<span data-ttu-id="5e360-115">Der Befehl speichert den Wert in der $value Variablen.</span><span class="sxs-lookup"><span data-stu-id="5e360-115">The command stores the value in the $value variable.</span></span>

## <span data-ttu-id="5e360-116">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="5e360-116">PARAMETERS</span></span>

### <span data-ttu-id="5e360-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5e360-117">-AutomationAccountName</span></span>
<span data-ttu-id="5e360-118">Gibt den Namen des Automatisierungskontos an, das die Variablen enthält, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5e360-118">Specifies the name of the Automation account that contains the variables that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5e360-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e360-119">-DefaultProfile</span></span>
<span data-ttu-id="5e360-120">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5e360-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5e360-121">-Name</span><span class="sxs-lookup"><span data-stu-id="5e360-121">-Name</span></span>
<span data-ttu-id="5e360-122">Gibt den Namen einer Variablen an, die dieses Cmdlet erhält.</span><span class="sxs-lookup"><span data-stu-id="5e360-122">Specifies the name of a variable that this cmdlet gets.</span></span>

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

### <span data-ttu-id="5e360-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e360-123">-ResourceGroupName</span></span>
<span data-ttu-id="5e360-124">Gibt die Ressourcengruppe an, für die dieses Cmdlet Variablen erhält.</span><span class="sxs-lookup"><span data-stu-id="5e360-124">Specifies the resource group for which this cmdlet gets variables.</span></span>

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

### <span data-ttu-id="5e360-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e360-125">CommonParameters</span></span>
<span data-ttu-id="5e360-126">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e360-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e360-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e360-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e360-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5e360-128">INPUTS</span></span>

### <span data-ttu-id="5e360-129">System.String</span><span class="sxs-lookup"><span data-stu-id="5e360-129">System.String</span></span>

## <span data-ttu-id="5e360-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5e360-130">OUTPUTS</span></span>

### <span data-ttu-id="5e360-131">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="5e360-131">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="5e360-132">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="5e360-132">NOTES</span></span>

## <span data-ttu-id="5e360-133">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="5e360-133">RELATED LINKS</span></span>

[<span data-ttu-id="5e360-134">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5e360-134">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="5e360-135">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5e360-135">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)

[<span data-ttu-id="5e360-136">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="5e360-136">Set-AzAutomationVariable</span></span>](./Set-AzAutomationVariable.md)


