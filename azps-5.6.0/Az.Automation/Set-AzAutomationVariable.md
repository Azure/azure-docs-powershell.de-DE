---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: ff83049e6afec5b0a6712aef2622bd9cbe0110c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101945341"
---
# <span data-ttu-id="1d4fb-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1d4fb-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="1d4fb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d4fb-102">SYNOPSIS</span></span>
<span data-ttu-id="1d4fb-103">Ändert eine Automatisierungsvariable.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="1d4fb-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1d4fb-104">SYNTAX</span></span>

### <span data-ttu-id="1d4fb-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="1d4fb-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1d4fb-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="1d4fb-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1d4fb-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1d4fb-107">DESCRIPTION</span></span>
<span data-ttu-id="1d4fb-108">Das **Cmdlet Set-AzAutomationVariable** ändert den Wert oder die Beschreibung einer Variablen in Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="1d4fb-109">Um die Variable zu verschlüsseln, geben Sie den *Parameter Verschlüsselt* an.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="1d4fb-110">Sie können den verschlüsselten Zustand einer Variablen nach der Erstellung nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="1d4fb-111">Das Angeben *von Verschlüsselt* für eine vorhandene, nicht verschlüsselte Variable schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="1d4fb-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1d4fb-112">EXAMPLES</span></span>

### <span data-ttu-id="1d4fb-113">Beispiel 1: Festlegen des Werts einer Variablen</span><span class="sxs-lookup"><span data-stu-id="1d4fb-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="1d4fb-114">Mit diesem Befehl wird ein neuer Wert für die Variable "StringVariable22" im Azure Automation-Konto namens Contoso17 bestimmt.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="1d4fb-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1d4fb-115">PARAMETERS</span></span>

### <span data-ttu-id="1d4fb-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1d4fb-116">-AutomationAccountName</span></span>
<span data-ttu-id="1d4fb-117">Gibt den Namen des Automatisierungskontos an, in dem die Variable gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="1d4fb-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d4fb-118">-DefaultProfile</span></span>
<span data-ttu-id="1d4fb-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="1d4fb-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1d4fb-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1d4fb-120">-Description</span></span>
<span data-ttu-id="1d4fb-121">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-121">Specifies a description for the variable.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVariableDescription
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d4fb-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="1d4fb-122">-Encrypted</span></span>
<span data-ttu-id="1d4fb-123">Gibt an, ob das Cmdlet den Wert der Variablen für den Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

```yaml
Type: System.Boolean
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d4fb-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1d4fb-124">-Name</span></span>
<span data-ttu-id="1d4fb-125">Gibt den Namen der Variablen an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="1d4fb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1d4fb-126">-ResourceGroupName</span></span>
<span data-ttu-id="1d4fb-127">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable ändert.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="1d4fb-128">-Wert</span><span class="sxs-lookup"><span data-stu-id="1d4fb-128">-Value</span></span>
<span data-ttu-id="1d4fb-129">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-129">Specifies a value for the variable.</span></span>

```yaml
Type: System.Object
Parameter Sets: UpdateVariableValue
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1d4fb-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d4fb-130">CommonParameters</span></span>
<span data-ttu-id="1d4fb-131">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d4fb-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d4fb-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1d4fb-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d4fb-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1d4fb-133">INPUTS</span></span>

### <span data-ttu-id="1d4fb-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1d4fb-134">System.String</span></span>

### <span data-ttu-id="1d4fb-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1d4fb-135">System.Boolean</span></span>

### <span data-ttu-id="1d4fb-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="1d4fb-136">System.Object</span></span>

## <span data-ttu-id="1d4fb-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1d4fb-137">OUTPUTS</span></span>

### <span data-ttu-id="1d4fb-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="1d4fb-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="1d4fb-139">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1d4fb-139">NOTES</span></span>

## <span data-ttu-id="1d4fb-140">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1d4fb-140">RELATED LINKS</span></span>

[<span data-ttu-id="1d4fb-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1d4fb-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="1d4fb-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1d4fb-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="1d4fb-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="1d4fb-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


