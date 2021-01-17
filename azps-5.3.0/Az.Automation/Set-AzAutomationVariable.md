---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: F344D8D1-5593-4C09-A1CA-37579D2A3A61
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationvariable
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationVariable.md
ms.openlocfilehash: 0ca1e99b68f7cca8d39647357ee81770ea41cefc
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471239"
---
# <span data-ttu-id="07bfc-101">Set-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="07bfc-101">Set-AzAutomationVariable</span></span>

## <span data-ttu-id="07bfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07bfc-102">SYNOPSIS</span></span>
<span data-ttu-id="07bfc-103">Ändert eine Automatisierungsvariable.</span><span class="sxs-lookup"><span data-stu-id="07bfc-103">Modifies an Automation variable.</span></span>

## <span data-ttu-id="07bfc-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="07bfc-104">SYNTAX</span></span>

### <span data-ttu-id="07bfc-105">UpdateVariableValue</span><span class="sxs-lookup"><span data-stu-id="07bfc-105">UpdateVariableValue</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Encrypted <Boolean> -Value <Object> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="07bfc-106">UpdateVariableDescription</span><span class="sxs-lookup"><span data-stu-id="07bfc-106">UpdateVariableDescription</span></span>
```
Set-AzAutomationVariable [-Name] <String> -Description <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="07bfc-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="07bfc-107">DESCRIPTION</span></span>
<span data-ttu-id="07bfc-108">Das **Cmdlet "Set-AzAutomationVariable"** ändert den Wert oder die Beschreibung einer Variablen in der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="07bfc-108">The **Set-AzAutomationVariable** cmdlet modifies the value or description of a variable in Azure Automation.</span></span>
<span data-ttu-id="07bfc-109">Um die Variable zu verschlüsseln, geben Sie den Parameter *"Encrypted"* an.</span><span class="sxs-lookup"><span data-stu-id="07bfc-109">To encrypt the variable, specify the *Encrypted* parameter.</span></span>
<span data-ttu-id="07bfc-110">Sie können den verschlüsselten Zustand einer Variablen nach der Erstellung nicht mehr ändern.</span><span class="sxs-lookup"><span data-stu-id="07bfc-110">You cannot modify the encrypted state of a variable after creation.</span></span>
<span data-ttu-id="07bfc-111">Die Angabe *"Verschlüsselt"* für eine vorhandene, nicht verschlüsselte Variable schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="07bfc-111">Specifying *Encrypted* for an existing, non-encrypted, variable fails.</span></span>

## <span data-ttu-id="07bfc-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="07bfc-112">EXAMPLES</span></span>

### <span data-ttu-id="07bfc-113">Beispiel 1: Festlegen des Werts einer Variablen</span><span class="sxs-lookup"><span data-stu-id="07bfc-113">Example 1: Set the value of a variable</span></span>
```
PS C:\>Set-AzAutomationVariable -AutomationAccountName "Contoso17" -Name "StringVariable22" -ResourceGroupName "ResourceGroup01" -Value "New Value" -Encrypted $False
```

<span data-ttu-id="07bfc-114">Dieser Befehl legt einen neuen Wert für die Variable "StringVariable22" im Azure-Automatisierungskonto namens "Contoso17" fest.</span><span class="sxs-lookup"><span data-stu-id="07bfc-114">This command sets a new value for the variable named StringVariable22 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="07bfc-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="07bfc-115">PARAMETERS</span></span>

### <span data-ttu-id="07bfc-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="07bfc-116">-AutomationAccountName</span></span>
<span data-ttu-id="07bfc-117">Gibt den Namen des Automatisierungskontos an, in dem die Variable gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="07bfc-117">Specifies the name of the Automation account in which the variable is stored.</span></span>

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

### <span data-ttu-id="07bfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07bfc-118">-DefaultProfile</span></span>
<span data-ttu-id="07bfc-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="07bfc-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="07bfc-120">-Beschreibung</span><span class="sxs-lookup"><span data-stu-id="07bfc-120">-Description</span></span>
<span data-ttu-id="07bfc-121">Gibt eine Beschreibung für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="07bfc-121">Specifies a description for the variable.</span></span>

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

### <span data-ttu-id="07bfc-122">-Encrypted</span><span class="sxs-lookup"><span data-stu-id="07bfc-122">-Encrypted</span></span>
<span data-ttu-id="07bfc-123">Gibt an, ob das Cmdlet den Wert der Variablen für den Speicher verschlüsselt.</span><span class="sxs-lookup"><span data-stu-id="07bfc-123">Specifies whether cmdlet encrypts the value of the variable for storage.</span></span>

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

### <span data-ttu-id="07bfc-124">-Name</span><span class="sxs-lookup"><span data-stu-id="07bfc-124">-Name</span></span>
<span data-ttu-id="07bfc-125">Gibt den Namen der Variablen an, die von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="07bfc-125">Specifies the name of the variable that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="07bfc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07bfc-126">-ResourceGroupName</span></span>
<span data-ttu-id="07bfc-127">Gibt die Ressourcengruppe an, für die dieses Cmdlet eine Variable ändert.</span><span class="sxs-lookup"><span data-stu-id="07bfc-127">Specifies the resource group for which this cmdlet modifies a variable.</span></span>

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

### <span data-ttu-id="07bfc-128">-Value</span><span class="sxs-lookup"><span data-stu-id="07bfc-128">-Value</span></span>
<span data-ttu-id="07bfc-129">Gibt einen Wert für die Variable an.</span><span class="sxs-lookup"><span data-stu-id="07bfc-129">Specifies a value for the variable.</span></span>

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

### <span data-ttu-id="07bfc-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07bfc-130">CommonParameters</span></span>
<span data-ttu-id="07bfc-131">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="07bfc-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07bfc-132">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07bfc-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07bfc-133">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="07bfc-133">INPUTS</span></span>

### <span data-ttu-id="07bfc-134">System.String</span><span class="sxs-lookup"><span data-stu-id="07bfc-134">System.String</span></span>

### <span data-ttu-id="07bfc-135">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="07bfc-135">System.Boolean</span></span>

### <span data-ttu-id="07bfc-136">System.Object</span><span class="sxs-lookup"><span data-stu-id="07bfc-136">System.Object</span></span>

## <span data-ttu-id="07bfc-137">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="07bfc-137">OUTPUTS</span></span>

### <span data-ttu-id="07bfc-138">Microsoft.Azure.Commands.Automation.Model.Variable</span><span class="sxs-lookup"><span data-stu-id="07bfc-138">Microsoft.Azure.Commands.Automation.Model.Variable</span></span>

## <span data-ttu-id="07bfc-139">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="07bfc-139">NOTES</span></span>

## <span data-ttu-id="07bfc-140">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="07bfc-140">RELATED LINKS</span></span>

[<span data-ttu-id="07bfc-141">Get-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="07bfc-141">Get-AzAutomationVariable</span></span>](./Get-AzAutomationVariable.md)

[<span data-ttu-id="07bfc-142">New-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="07bfc-142">New-AzAutomationVariable</span></span>](./New-AzAutomationVariable.md)

[<span data-ttu-id="07bfc-143">Remove-AzAutomationVariable</span><span class="sxs-lookup"><span data-stu-id="07bfc-143">Remove-AzAutomationVariable</span></span>](./Remove-AzAutomationVariable.md)


