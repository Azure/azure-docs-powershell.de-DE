---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: E4FC60AE-16B4-4E62-874F-49B9285CFF7A
online version: https://docs.microsoft.com/powershell/module/az.automation/unregister-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Unregister-AzAutomationDscNode.md
ms.openlocfilehash: 5c8d58024f14e2dbd1be929ddb6f156b479d2487
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101938299"
---
# <span data-ttu-id="d46d7-101">Unregister-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d46d7-101">Unregister-AzAutomationDscNode</span></span>

## <span data-ttu-id="d46d7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d46d7-102">SYNOPSIS</span></span>
<span data-ttu-id="d46d7-103">Entfernt einen DSC-Knoten aus der Verwaltung durch ein Automatisierungskonto.</span><span class="sxs-lookup"><span data-stu-id="d46d7-103">Removes a DSC node from management by an Automation account.</span></span>

## <span data-ttu-id="d46d7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="d46d7-104">SYNTAX</span></span>

```
Unregister-AzAutomationDscNode -Id <Guid> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d46d7-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="d46d7-105">DESCRIPTION</span></span>
<span data-ttu-id="d46d7-106">Das **Cmdlet "Unregister-AzAutomationDscNode"** entfernt einen APS Desired State Configuration (DSC)-Knoten aus der Verwaltung durch ein Azure Automation-Konto.</span><span class="sxs-lookup"><span data-stu-id="d46d7-106">The **Unregister-AzAutomationDscNode** cmdlet removes an APS Desired State Configuration (DSC) node from management by an Azure Automation account.</span></span>

## <span data-ttu-id="d46d7-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="d46d7-107">EXAMPLES</span></span>

### <span data-ttu-id="d46d7-108">Beispiel 1: Entfernen eines Azure DSC-Knotens aus der Verwaltung durch ein Automatisierungskonto</span><span class="sxs-lookup"><span data-stu-id="d46d7-108">Example 1: Remove an Azure DSC node from management by an Automation account</span></span>
```
PS C:\>Unregister-AzAutomationDscNode -AutomationAccountName "Contoso17" -ResourceGroupName "ResourceGroup01" -Id 064a8929-c98b-25e4-80hh-111ca86067j8
```

<span data-ttu-id="d46d7-109">Mit diesem Befehl wird der DSC-Knoten mit der angegebenen GUID aus der Verwaltung durch das Automatisierungskonto namens Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="d46d7-109">This command removes the DSC node that has the specified GUID from management by the Automation account named Contoso17.</span></span>

## <span data-ttu-id="d46d7-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="d46d7-110">PARAMETERS</span></span>

### <span data-ttu-id="d46d7-111">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="d46d7-111">-AutomationAccountName</span></span>
<span data-ttu-id="d46d7-112">Gibt den Namen des Automatisierungskontos an, aus dem dieses Cmdlet einen DSC-Knoten entfernt.</span><span class="sxs-lookup"><span data-stu-id="d46d7-112">Specifies the name of the Automation account from which this cmdlet removes a DSC node.</span></span>

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

### <span data-ttu-id="d46d7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d46d7-113">-DefaultProfile</span></span>
<span data-ttu-id="d46d7-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="d46d7-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d46d7-115">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="d46d7-115">-Force</span></span>
<span data-ttu-id="d46d7-116">ps_force</span><span class="sxs-lookup"><span data-stu-id="d46d7-116">ps_force</span></span>

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

### <span data-ttu-id="d46d7-117">-ID</span><span class="sxs-lookup"><span data-stu-id="d46d7-117">-Id</span></span>
<span data-ttu-id="d46d7-118">Gibt die eindeutige ID des DSC-Knotens an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="d46d7-118">Specifies the unique ID of the DSC node that this cmdlet removes.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: NodeId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d46d7-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d46d7-119">-ResourceGroupName</span></span>
<span data-ttu-id="d46d7-120">Gibt den Namen einer Ressourcengruppe an, in der dieses Cmdlet die Registrierung eines DSC-Knotens aufgibt.</span><span class="sxs-lookup"><span data-stu-id="d46d7-120">Specifies the name of a resource group in which this cmdlet unregisters a DSC node.</span></span>

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

### <span data-ttu-id="d46d7-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d46d7-121">-Confirm</span></span>
<span data-ttu-id="d46d7-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d46d7-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d46d7-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d46d7-123">-WhatIf</span></span>
<span data-ttu-id="d46d7-124">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d46d7-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d46d7-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d46d7-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d46d7-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d46d7-126">CommonParameters</span></span>
<span data-ttu-id="d46d7-127">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d46d7-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d46d7-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d46d7-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d46d7-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="d46d7-129">INPUTS</span></span>

### <span data-ttu-id="d46d7-130">System.Guid</span><span class="sxs-lookup"><span data-stu-id="d46d7-130">System.Guid</span></span>

### <span data-ttu-id="d46d7-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d46d7-131">System.String</span></span>

## <span data-ttu-id="d46d7-132">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="d46d7-132">OUTPUTS</span></span>

### <span data-ttu-id="d46d7-133">Microsoft.Azure.Commands.Automation.Model.Dscnode</span><span class="sxs-lookup"><span data-stu-id="d46d7-133">Microsoft.Azure.Commands.Automation.Model.DscNode</span></span>

## <span data-ttu-id="d46d7-134">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="d46d7-134">NOTES</span></span>

## <span data-ttu-id="d46d7-135">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="d46d7-135">RELATED LINKS</span></span>

[<span data-ttu-id="d46d7-136">Get-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d46d7-136">Get-AzAutomationDscNode</span></span>](./Get-AzAutomationDscNode.md)

[<span data-ttu-id="d46d7-137">Register-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d46d7-137">Register-AzAutomationDscNode</span></span>](./Register-AzAutomationDscNode.md)

[<span data-ttu-id="d46d7-138">Set-AzAutomationDscNode</span><span class="sxs-lookup"><span data-stu-id="d46d7-138">Set-AzAutomationDscNode</span></span>](./Set-AzAutomationDscNode.md)


