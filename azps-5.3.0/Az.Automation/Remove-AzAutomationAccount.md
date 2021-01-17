---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 515933DF-5DB1-452A-808B-0198A3A2EA8B
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationAccount.md
ms.openlocfilehash: d3f76fe1e1c482c8d2913266e9c40dc5b41c62f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471293"
---
# <span data-ttu-id="ef22d-101">Remove-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef22d-101">Remove-AzAutomationAccount</span></span>

## <span data-ttu-id="ef22d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef22d-102">SYNOPSIS</span></span>
<span data-ttu-id="ef22d-103">Entfernt ein Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="ef22d-103">Removes an Automation account.</span></span>

## <span data-ttu-id="ef22d-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="ef22d-104">SYNTAX</span></span>

```
Remove-AzAutomationAccount [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef22d-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="ef22d-105">DESCRIPTION</span></span>
<span data-ttu-id="ef22d-106">Das **Cmdlet "Remove-AzAutomationAccount"** entfernt ein Azure-Automatisierungskonto aus einer Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="ef22d-106">The **Remove-AzAutomationAccount** cmdlet removes an Azure Automation account from a resource group.</span></span>
<span data-ttu-id="ef22d-107">Weitere Informationen zu Automatisierungskonten finden Sie im New-AzAutomationAccount-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ef22d-107">For more information about Automation accounts, see the New-AzAutomationAccount cmdlet.</span></span>

## <span data-ttu-id="ef22d-108">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="ef22d-108">EXAMPLES</span></span>

### <span data-ttu-id="ef22d-109">Beispiel 1: Entfernen eines Automatisierungskontos</span><span class="sxs-lookup"><span data-stu-id="ef22d-109">Example 1: Remove an automation account</span></span>
```
PS C:\>Remove-AzAutomationAccount -Name "ContosoAutomationAccount" -Force -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="ef22d-110">Mit diesem Befehl wird ein Automatisierungskonto namens "ContosoAutomationAccount" entfernt, ohne dass zur Benutzerüberprüfung aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="ef22d-110">This command removes an automation account named ContosoAutomationAccount without prompting for user validation.</span></span>

## <span data-ttu-id="ef22d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ef22d-111">PARAMETERS</span></span>

### <span data-ttu-id="ef22d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef22d-112">-DefaultProfile</span></span>
<span data-ttu-id="ef22d-113">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="ef22d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ef22d-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ef22d-114">-Force</span></span>
<span data-ttu-id="ef22d-115">ps_force</span><span class="sxs-lookup"><span data-stu-id="ef22d-115">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef22d-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ef22d-116">-Name</span></span>
<span data-ttu-id="ef22d-117">Gibt den Namen des Automatisierungskontos an, das von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="ef22d-117">Specifies the name of the Automation account that this cmdlet removes.</span></span>

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

### <span data-ttu-id="ef22d-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef22d-118">-ResourceGroupName</span></span>
<span data-ttu-id="ef22d-119">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet ein Automatisierungskonto entfernt.</span><span class="sxs-lookup"><span data-stu-id="ef22d-119">Specifies the name of the resource group from which this cmdlet removes an Automation account.</span></span>

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

### <span data-ttu-id="ef22d-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ef22d-120">-Confirm</span></span>
<span data-ttu-id="ef22d-121">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="ef22d-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef22d-122">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="ef22d-122">-WhatIf</span></span>
<span data-ttu-id="ef22d-123">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ef22d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ef22d-124">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="ef22d-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef22d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef22d-125">CommonParameters</span></span>
<span data-ttu-id="ef22d-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ef22d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef22d-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef22d-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef22d-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="ef22d-128">INPUTS</span></span>

### <span data-ttu-id="ef22d-129">System.String</span><span class="sxs-lookup"><span data-stu-id="ef22d-129">System.String</span></span>

## <span data-ttu-id="ef22d-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="ef22d-130">OUTPUTS</span></span>

### <span data-ttu-id="ef22d-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef22d-131">Microsoft.Azure.Commands.Automation.Model.AutomationAccount</span></span>

## <span data-ttu-id="ef22d-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="ef22d-132">NOTES</span></span>

## <span data-ttu-id="ef22d-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="ef22d-133">RELATED LINKS</span></span>

[<span data-ttu-id="ef22d-134">Get-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef22d-134">Get-AzAutomationAccount</span></span>](./Get-AzAutomationAccount.md)

[<span data-ttu-id="ef22d-135">New-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef22d-135">New-AzAutomationAccount</span></span>](./New-AzAutomationAccount.md)

[<span data-ttu-id="ef22d-136">Set-AzAutomationAccount</span><span class="sxs-lookup"><span data-stu-id="ef22d-136">Set-AzAutomationAccount</span></span>](./Set-AzAutomationAccount.md)


