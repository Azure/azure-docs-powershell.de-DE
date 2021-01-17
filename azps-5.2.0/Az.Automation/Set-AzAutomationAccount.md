---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: B1897EFC-0184-4A8B-B8E4-203CC8E3B179
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationAccount.md
ms.openlocfilehash: f32e9c0d76e88fba5475abb39595b0a6c4bea834
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373146"
---
# <span data-ttu-id="5da27-101">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5da27-101">Set-AzAutomationAccount</span></span>

## <span data-ttu-id="5da27-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da27-102">SYNOPSIS</span></span>
<span data-ttu-id="5da27-103">Ändert ein Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="5da27-103">Modifies an Automation account.</span></span>

## <span data-ttu-id="5da27-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5da27-104">SYNTAX</span></span>

```
Set-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Plan <String>] [-Tags <IDictionary>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da27-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5da27-105">DESCRIPTION</span></span>
<span data-ttu-id="5da27-106">Das **Cmdlet Set-AzAutomationAccount** ändert ein Azure-Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="5da27-106">The **Set-AzAutomationAccount** cmdlet modifies an Azure Automation account.</span></span>
<span data-ttu-id="5da27-107">Weitere Informationen zu Automatisierungskonten finden Sie im New-AzAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5da27-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="5da27-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5da27-108">EXAMPLES</span></span>

### <span data-ttu-id="5da27-109">Beispiel 1: Festlegen der Tags für ein Automatisierungskonto</span><span class="sxs-lookup"><span data-stu-id="5da27-109">Example 1: Set the tags for an Automation account</span></span>
```
PS C:\>$Tags = @{"tag01"="value01";"tag02"="value02"}
PS C:\> Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Tags $Tags
```

<span data-ttu-id="5da27-110">Der erste Befehl weist der Variablen zwei Schlüssel/Wert-Paare $Tags zu.</span><span class="sxs-lookup"><span data-stu-id="5da27-110">The first command assigns two key/value pairs to the $Tags variable.</span></span>
<span data-ttu-id="5da27-111">Der zweite Befehl legt Tags in der $Tags für das Automatisierungskonto namens AutomationAccount01 fest.</span><span class="sxs-lookup"><span data-stu-id="5da27-111">The second command sets tags in $Tags for the Automation account named AutomationAccount01.</span></span>

### <span data-ttu-id="5da27-112">Beispiel 2: Ändern des Plans für ein Automatisierungskonto</span><span class="sxs-lookup"><span data-stu-id="5da27-112">Example 2: Change the plan for an Automation account</span></span>
```
PS C:\>Set-AzAutomationAccount -Name "AutomationAccount01" -ResourceGroupName "ResourceGroup01" -Plan Basic
```

<span data-ttu-id="5da27-113">Mit diesem Befehl wird der Plan in "Basic" für das Automatisierungskonto namens "AutomationAccount01" geändert.</span><span class="sxs-lookup"><span data-stu-id="5da27-113">This command changes the plan to Basic for the Automation account named AutomationAccount01.</span></span>

## <span data-ttu-id="5da27-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5da27-114">PARAMETERS</span></span>

### <span data-ttu-id="5da27-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da27-115">-DefaultProfile</span></span>
<span data-ttu-id="5da27-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5da27-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5da27-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5da27-117">-Name</span></span>
<span data-ttu-id="5da27-118">Gibt den Namen des Automatisierungskontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5da27-118">Specifies the name of the Automation account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AutomationAccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da27-119">-Plan</span><span class="sxs-lookup"><span data-stu-id="5da27-119">-Plan</span></span>
<span data-ttu-id="5da27-120">Gibt den Plan für das Automatisierungskonto an.</span><span class="sxs-lookup"><span data-stu-id="5da27-120">Specifies the plan for the Automation account.</span></span>
<span data-ttu-id="5da27-121">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="5da27-121">Valid values are:</span></span>
- <span data-ttu-id="5da27-122">Standard</span><span class="sxs-lookup"><span data-stu-id="5da27-122">Basic</span></span>
- <span data-ttu-id="5da27-123">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="5da27-123">Free</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da27-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5da27-124">-ResourceGroupName</span></span>
<span data-ttu-id="5da27-125">Gibt den Namen einer Ressourcengruppe an, die das Automatisierungskonto enthält, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5da27-125">Specifies the name of a resource group that contains the Automation account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="5da27-126">-Tags</span><span class="sxs-lookup"><span data-stu-id="5da27-126">-Tags</span></span>
<span data-ttu-id="5da27-127">Schlüssel-Wert-Paare in Form einer Hashtabelle.</span><span class="sxs-lookup"><span data-stu-id="5da27-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="5da27-128">Beispiel: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5da27-128">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.IDictionary
Parameter Sets: (All)
Aliases: Tag

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5da27-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da27-129">CommonParameters</span></span>
<span data-ttu-id="5da27-130">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5da27-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da27-131">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da27-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da27-132">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5da27-132">INPUTS</span></span>

### <span data-ttu-id="5da27-133">System.String</span><span class="sxs-lookup"><span data-stu-id="5da27-133">System.String</span></span>

### <span data-ttu-id="5da27-134">System.Collections.IDictionary</span><span class="sxs-lookup"><span data-stu-id="5da27-134">System.Collections.IDictionary</span></span>

## <span data-ttu-id="5da27-135">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5da27-135">OUTPUTS</span></span>

### <span data-ttu-id="5da27-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5da27-136">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="5da27-137">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5da27-137">NOTES</span></span>

## <span data-ttu-id="5da27-138">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5da27-138">RELATED LINKS</span></span>

[<span data-ttu-id="5da27-139">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5da27-139">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="5da27-140">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5da27-140">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="5da27-141">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="5da27-141">Remove-AzAutomationAccount</span></span>](./Remove-AzAutomationAccount.md)
