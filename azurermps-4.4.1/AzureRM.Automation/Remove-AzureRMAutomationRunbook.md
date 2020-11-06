---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 16055879-C001-46E7-B8C3-1FE2A1A67AC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Remove-AzureRMAutomationRunbook.md
ms.openlocfilehash: 96a82f4cc39952517bf5cfaeca24191cc4dd2d9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499234"
---
# <span data-ttu-id="2a427-101">Remove-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-101">Remove-AzureRmAutomationRunbook</span></span>

## <span data-ttu-id="2a427-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2a427-102">SYNOPSIS</span></span>
<span data-ttu-id="2a427-103">Entfernt eine runbooks.</span><span class="sxs-lookup"><span data-stu-id="2a427-103">Removes a runbook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2a427-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2a427-104">SYNTAX</span></span>

```
Remove-AzureRmAutomationRunbook [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="2a427-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2a427-105">DESCRIPTION</span></span>
<span data-ttu-id="2a427-106">Mit dem Cmdlet **Remove-AzureRmAutomationRunbook** wird ein runbooks aus Azure Automation entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a427-106">The **Remove-AzureRmAutomationRunbook** cmdlet removes a runbook from Azure Automation.</span></span>

## <span data-ttu-id="2a427-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2a427-107">EXAMPLES</span></span>

### <span data-ttu-id="2a427-108">Beispiel 1: Entfernen eines runbooks</span><span class="sxs-lookup"><span data-stu-id="2a427-108">Example 1: Remove a runbook</span></span>
```
PS C:\>Remove-AzureRmAutomationRunbook -AutomationAccountName "Contoso17" -Name "Runbook03" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="2a427-109">Dieser Befehl entfernt das runbooks mit dem Namen Runbook03 im Azure Automation-Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="2a427-109">This command removes the runbook named Runbook03 in the Azure Automation account named Contoso17.</span></span>

## <span data-ttu-id="2a427-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="2a427-110">PARAMETERS</span></span>

### <span data-ttu-id="2a427-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="2a427-111">-AutomationAccountName</span></span>
<span data-ttu-id="2a427-112">Gibt den Namen des Automatisierungs Kontos an, in dem dieses Cmdlet eine runbooks entfernt.</span><span class="sxs-lookup"><span data-stu-id="2a427-112">Specifies the name of the Automation account in which this cmdlet removes a runbook.</span></span>

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

### <span data-ttu-id="2a427-113">-Force</span><span class="sxs-lookup"><span data-stu-id="2a427-113">-Force</span></span>
<span data-ttu-id="2a427-114">ps_force</span><span class="sxs-lookup"><span data-stu-id="2a427-114">ps_force</span></span>

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

### <span data-ttu-id="2a427-115">-Name</span><span class="sxs-lookup"><span data-stu-id="2a427-115">-Name</span></span>
<span data-ttu-id="2a427-116">Gibt den Namen der runbooks an, die von diesem Cmdlet entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="2a427-116">Specifies the name of the runbook that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: RunbookName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2a427-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2a427-117">-ResourceGroupName</span></span>
<span data-ttu-id="2a427-118">Gibt den Namen der Ressourcengruppe an, für die dieses Cmdlet eine runbooks veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="2a427-118">Specifies the name of the resource group for which this cmdlet publishes a runbook.</span></span>

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

### <span data-ttu-id="2a427-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2a427-119">-Confirm</span></span>
<span data-ttu-id="2a427-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a427-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2a427-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2a427-121">-WhatIf</span></span>
<span data-ttu-id="2a427-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2a427-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2a427-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2a427-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2a427-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a427-124">-DefaultProfile</span></span>
<span data-ttu-id="2a427-125">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="2a427-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2a427-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a427-126">CommonParameters</span></span>
<span data-ttu-id="2a427-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2a427-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a427-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2a427-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a427-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2a427-129">INPUTS</span></span>

## <span data-ttu-id="2a427-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2a427-130">OUTPUTS</span></span>

## <span data-ttu-id="2a427-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="2a427-131">NOTES</span></span>

## <span data-ttu-id="2a427-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2a427-132">RELATED LINKS</span></span>

[<span data-ttu-id="2a427-133">Export-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-133">Export-AzureRmAutomationRunbook</span></span>](./Export-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-134">Get-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-134">Get-AzureRmAutomationRunbook</span></span>](./Get-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-135">Importieren-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-135">Import-AzureRmAutomationRunbook</span></span>](./Import-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-136">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-136">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-137">Neu – AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-137">New-AzureRmAutomationRunbook</span></span>](./New-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-138">Publish-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-138">Publish-AzureRmAutomationRunbook</span></span>](./Publish-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-139">Satz-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-139">Set-AzureRmAutomationRunbook</span></span>](./Set-AzureRMAutomationRunbook.md)

[<span data-ttu-id="2a427-140">Anfang-AzureRmAutomationRunbook</span><span class="sxs-lookup"><span data-stu-id="2a427-140">Start-AzureRmAutomationRunbook</span></span>](./Start-AzureRMAutomationRunbook.md)


