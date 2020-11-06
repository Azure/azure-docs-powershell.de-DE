---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: EAD39EE1-C66F-4092-8876-E7F9FA612481
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/remove-azurermautomationschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationSchedule.md
ms.openlocfilehash: 83481e1d12782c3381c2d5923aa610072da41d9a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504585"
---
# <span data-ttu-id="5f0e1-101">Remove-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5f0e1-101">Remove-AzureRmAutomationSchedule</span></span>

## <span data-ttu-id="5f0e1-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5f0e1-102">SYNOPSIS</span></span>
<span data-ttu-id="5f0e1-103">Löscht einen Automatisierungs Zeitplan.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-103">Deletes an Automation schedule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f0e1-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5f0e1-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationSchedule [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5f0e1-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5f0e1-105">DESCRIPTION</span></span>
<span data-ttu-id="5f0e1-106">Das Cmdlet **Remove-AzureRmAutomationSchedule** löscht einen Zeitplan aus der Azure-Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-106">The **Remove-AzureRmAutomationSchedule** cmdlet deletes a schedule from Azure Automation.</span></span>

## <span data-ttu-id="5f0e1-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5f0e1-107">EXAMPLES</span></span>

### <span data-ttu-id="5f0e1-108">Beispiel 1: Entfernen eines Zeitplans</span><span class="sxs-lookup"><span data-stu-id="5f0e1-108">Example 1: Remove a schedule</span></span>
```
PS C:\>Remove-AzureRmAutomationSchedule -AutomationAccountName "Contoso17" -Name "Schedule01" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="5f0e1-109">Mit diesem Befehl wird die Beschreibung des Zeitplans mit dem Namen Schedule01 geändert.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-109">This command modifies the description of the schedule named Schedule01.</span></span>

## <span data-ttu-id="5f0e1-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="5f0e1-110">PARAMETERS</span></span>

### <span data-ttu-id="5f0e1-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5f0e1-111">-AutomationAccountName</span></span>
<span data-ttu-id="5f0e1-112">Gibt den Namen eines Automatisierungs Kontos an, für das mit diesem Cmdlet ein Zeitplan geändert wird.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-112">Specifies the name of an Automation account for which this cmdlet modifies a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f0e1-113">-DefaultProfile</span></span>
<span data-ttu-id="5f0e1-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="5f0e1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5f0e1-115">-Force</span></span>
<span data-ttu-id="5f0e1-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="5f0e1-116">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="5f0e1-117">-Name</span></span>
<span data-ttu-id="5f0e1-118">Gibt den Namen für den Zeitplan an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-118">Specifies the name for the schedule that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f0e1-119">-ResourceGroupName</span></span>
<span data-ttu-id="5f0e1-120">Gibt den Namen einer Ressourcengruppe an, für die dieses Cmdlet einen Terminplan entfernt.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-120">Specifies the name of a resource group for which this cmdlet removes a schedule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5f0e1-121">-Confirm</span></span>
<span data-ttu-id="5f0e1-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f0e1-123">-WhatIf</span></span>
<span data-ttu-id="5f0e1-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f0e1-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-125">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5f0e1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f0e1-126">CommonParameters</span></span>
<span data-ttu-id="5f0e1-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f0e1-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f0e1-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f0e1-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5f0e1-129">INPUTS</span></span>

### <span data-ttu-id="5f0e1-130">Keine</span><span class="sxs-lookup"><span data-stu-id="5f0e1-130">None</span></span>
<span data-ttu-id="5f0e1-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="5f0e1-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5f0e1-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5f0e1-132">OUTPUTS</span></span>

## <span data-ttu-id="5f0e1-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="5f0e1-133">NOTES</span></span>

## <span data-ttu-id="5f0e1-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5f0e1-134">RELATED LINKS</span></span>

[<span data-ttu-id="5f0e1-135">Get-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5f0e1-135">Get-AzureRmAutomationSchedule</span></span>](./Get-AzureRMAutomationSchedule.md)

[<span data-ttu-id="5f0e1-136">Neu – AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5f0e1-136">New-AzureRmAutomationSchedule</span></span>](./New-AzureRMAutomationSchedule.md)

[<span data-ttu-id="5f0e1-137">Satz-AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5f0e1-137">Set-AzureRmAutomationSchedule</span></span>](./Set-AzureRMAutomationSchedule.md)


