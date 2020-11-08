---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationhybridworkergroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationHybridWorkerGroup.md
ms.openlocfilehash: 78674e3245da1b8a58e099948bff23df9159efec
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005132"
---
# <span data-ttu-id="1306a-101">Remove-AzAutomationHybridWorkerGroup</span><span class="sxs-lookup"><span data-stu-id="1306a-101">Remove-AzAutomationHybridWorkerGroup</span></span>

## <span data-ttu-id="1306a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1306a-102">SYNOPSIS</span></span>
<span data-ttu-id="1306a-103">Entfernt eine Hybrid Arbeitskraft Gruppe aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="1306a-103">Removes hybrid worker group from Automation.</span></span>

## <span data-ttu-id="1306a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1306a-104">SYNTAX</span></span>

```
Remove-AzAutomationHybridWorkerGroup [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1306a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1306a-105">DESCRIPTION</span></span>
<span data-ttu-id="1306a-106">Das Remove-AzAutomationHybridWorkerGroup-Cmdlet entfernt eine Hybrid Arbeitskraft Gruppe aus Automatisierung.</span><span class="sxs-lookup"><span data-stu-id="1306a-106">The Remove-AzAutomationHybridWorkerGroup cmdlet removes a hybrid worker group from Automation.</span></span>

## <span data-ttu-id="1306a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1306a-107">EXAMPLES</span></span>

### <span data-ttu-id="1306a-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="1306a-108">Example 1</span></span>
<span data-ttu-id="1306a-109">Mit diesem Befehl wird ein Hybrid Worker nach Name entfernt.</span><span class="sxs-lookup"><span data-stu-id="1306a-109">This command removes a hybrid worker by name.</span></span>

```powershell
PS C:\> Remove-AzAutomationHybridWorkerGroup -ResourceGroupName "rg1" `
                                                  -AutomationAccountName "devAccount" `
                                                  -Name "GroupName" `
                                                  -Force
```

## <span data-ttu-id="1306a-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="1306a-110">PARAMETERS</span></span>

### <span data-ttu-id="1306a-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="1306a-111">-AutomationAccountName</span></span>
<span data-ttu-id="1306a-112">Der Name des Automatisierungs Kontos.</span><span class="sxs-lookup"><span data-stu-id="1306a-112">The automation account name.</span></span>

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

### <span data-ttu-id="1306a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1306a-113">-DefaultProfile</span></span>
<span data-ttu-id="1306a-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="1306a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1306a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="1306a-115">-Name</span></span>
<span data-ttu-id="1306a-116">Der Name der Hybrid Arbeitskraft Gruppe.</span><span class="sxs-lookup"><span data-stu-id="1306a-116">The hybrid worker group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Group

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1306a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1306a-117">-ResourceGroupName</span></span>
<span data-ttu-id="1306a-118">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="1306a-118">The resource group name.</span></span>

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

### <span data-ttu-id="1306a-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1306a-119">-Confirm</span></span>
<span data-ttu-id="1306a-120">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1306a-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306a-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1306a-121">-WhatIf</span></span>
<span data-ttu-id="1306a-122">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1306a-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1306a-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1306a-123">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1306a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1306a-124">CommonParameters</span></span>
<span data-ttu-id="1306a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1306a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1306a-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1306a-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1306a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1306a-127">INPUTS</span></span>

### <span data-ttu-id="1306a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="1306a-128">System.String</span></span>

## <span data-ttu-id="1306a-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1306a-129">OUTPUTS</span></span>

### <span data-ttu-id="1306a-130">System. void</span><span class="sxs-lookup"><span data-stu-id="1306a-130">System.Void</span></span>

## <span data-ttu-id="1306a-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="1306a-131">NOTES</span></span>

## <span data-ttu-id="1306a-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1306a-132">RELATED LINKS</span></span>
