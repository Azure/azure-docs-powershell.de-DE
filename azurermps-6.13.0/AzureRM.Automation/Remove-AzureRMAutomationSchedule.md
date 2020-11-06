---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: cce9b4eff96be34521af58ec85f7abb93d39b3cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500297"
---
# <span data-ttu-id="6fe64-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe64-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="6fe64-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="6fe64-102">SYNOPSIS</span></span>
<span data-ttu-id="6fe64-103">Löscht einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="6fe64-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6fe64-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="6fe64-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6fe64-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6fe64-105">DESCRIPTION</span></span>
<span data-ttu-id="6fe64-106">Das Cmdlet **Remove-AzureRmAutomationSchedule** löscht einen Zeitplan aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="6fe64-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="6fe64-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="6fe64-107">EXAMPLES</span></span>

### <span data-ttu-id="6fe64-108">Beispiel 1: Entfernen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="6fe64-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="6fe64-109">Dieser Befehl löscht den Zeitplan mit dem Namen Schedule01 in Automatisierungs Konto Contoso17 in der Ressourcengruppe ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="6fe64-109">This command deletes the schedule named Schedule01 in automation account Contoso17 in resource group ResourceGroup01.</span></span>

## <span data-ttu-id="6fe64-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="6fe64-110">PARAMETERS</span></span>

### <span data-ttu-id="6fe64-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6fe64-111">-AutomationAccountName</span></span>
<span data-ttu-id="6fe64-112">Gibt den Namen eines Automatisierungs Kontos an, für das dieses Cmdlet einen Terminplan entfernt.</span><span class="sxs-lookup"><span data-stu-id="6fe64-112">Specifies the name of an Automation account for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6fe64-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6fe64-113">-DefaultProfile</span></span>
<span data-ttu-id="6fe64-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="6fe64-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6fe64-115">-Force</span><span class="sxs-lookup"><span data-stu-id="6fe64-115">-Force</span></span>
<span data-ttu-id="6fe64-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="6fe64-116">ps_force</span></span>

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

### <span data-ttu-id="6fe64-117">-Name</span><span class="sxs-lookup"><span data-stu-id="6fe64-117">-Name</span></span>
<span data-ttu-id="6fe64-118">Gibt den Namen für den Zeitplan an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="6fe64-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

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

### <span data-ttu-id="6fe64-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6fe64-119">-ResourceGroupName</span></span>
<span data-ttu-id="6fe64-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Terminplan entfernt.</span><span class="sxs-lookup"><span data-stu-id="6fe64-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

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

### <span data-ttu-id="6fe64-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="6fe64-121">-Confirm</span></span>
<span data-ttu-id="6fe64-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="6fe64-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6fe64-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6fe64-123">-WhatIf</span></span>
<span data-ttu-id="6fe64-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6fe64-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6fe64-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6fe64-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6fe64-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6fe64-126">CommonParameters</span></span>
<span data-ttu-id="6fe64-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6fe64-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6fe64-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6fe64-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6fe64-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="6fe64-129">INPUTS</span></span>

### <span data-ttu-id="6fe64-130">System. String</span><span class="sxs-lookup"><span data-stu-id="6fe64-130">System.String</span></span>

## <span data-ttu-id="6fe64-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="6fe64-131">OUTPUTS</span></span>

### <span data-ttu-id="6fe64-132">System. void</span><span class="sxs-lookup"><span data-stu-id="6fe64-132">System.Void</span></span>

## <span data-ttu-id="6fe64-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="6fe64-133">NOTES</span></span>

## <span data-ttu-id="6fe64-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="6fe64-134">RELATED LINKS</span></span>

[<span data-ttu-id="6fe64-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe64-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6fe64-136">Neu – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe64-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="6fe64-137">Satz-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="6fe64-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


