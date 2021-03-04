---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 4d153a05ad245eeece671adced6aa2f8029dc9a2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101947595"
---
# <span data-ttu-id="a7123-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="a7123-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="a7123-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7123-102">SYNOPSIS</span></span>
<span data-ttu-id="a7123-103">Entfernt einen Automatisierungsverbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="a7123-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="a7123-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a7123-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a7123-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a7123-105">DESCRIPTION</span></span>
<span data-ttu-id="a7123-106">Das **Cmdlet Remove-AzAutomationConnectionType** entfernt einen Verbindungstyp aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="a7123-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="a7123-107">Alle Verbindungen, die dem verbindungstyp zugeordnet sind, den Sie löschen, werden unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="a7123-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="a7123-108">Entfernen Sie sie, es sei denn, Sie erstellen einen neuen Verbindungstyp, der die folgenden Kriterien erfüllt:</span><span class="sxs-lookup"><span data-stu-id="a7123-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="a7123-109">Der Typ hat denselben Namen wie der ursprüngliche Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="a7123-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="a7123-110">Der Typ hat die gleichen Felddefinitionen wie der ursprüngliche Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="a7123-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="a7123-111">Sie kann weitere Felder enthalten.</span><span class="sxs-lookup"><span data-stu-id="a7123-111">It can have additional fields.</span></span>

## <span data-ttu-id="a7123-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a7123-112">EXAMPLES</span></span>

### <span data-ttu-id="a7123-113">Beispiel 1: Entfernen eines Verbindungstyps</span><span class="sxs-lookup"><span data-stu-id="a7123-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="a7123-114">Mit diesem Befehl wird der Verbindungstyp ContosoConnectionType im Automatisierungskonto namens Contoso17 entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7123-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="a7123-115">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a7123-115">PARAMETERS</span></span>

### <span data-ttu-id="a7123-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a7123-116">-AutomationAccountName</span></span>
<span data-ttu-id="a7123-117">Gibt den Namen des Automatisierungskontos an, für das dieses Cmdlet einen Verbindungstyp entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7123-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="a7123-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7123-118">-DefaultProfile</span></span>
<span data-ttu-id="a7123-119">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a7123-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a7123-120">-Erzwingen</span><span class="sxs-lookup"><span data-stu-id="a7123-120">-Force</span></span>
<span data-ttu-id="a7123-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="a7123-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a7123-122">-Name</span><span class="sxs-lookup"><span data-stu-id="a7123-122">-Name</span></span>
<span data-ttu-id="a7123-123">Gibt den Namen des Verbindungstyps Automatisierung an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7123-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="a7123-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7123-124">-ResourceGroupName</span></span>
<span data-ttu-id="a7123-125">Gibt den Namen der Ressourcengruppe an, aus der dieses Cmdlet einen Verbindungstyp Automatisierung entfernt.</span><span class="sxs-lookup"><span data-stu-id="a7123-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="a7123-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a7123-126">-Confirm</span></span>
<span data-ttu-id="a7123-127">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a7123-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7123-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7123-128">-WhatIf</span></span>
<span data-ttu-id="a7123-129">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a7123-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a7123-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a7123-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7123-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7123-131">CommonParameters</span></span>
<span data-ttu-id="a7123-132">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a7123-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7123-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a7123-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7123-134">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a7123-134">INPUTS</span></span>

### <span data-ttu-id="a7123-135">System.String</span><span class="sxs-lookup"><span data-stu-id="a7123-135">System.String</span></span>

## <span data-ttu-id="a7123-136">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a7123-136">OUTPUTS</span></span>

### <span data-ttu-id="a7123-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="a7123-137">System.Void</span></span>

## <span data-ttu-id="a7123-138">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a7123-138">NOTES</span></span>

## <span data-ttu-id="a7123-139">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a7123-139">RELATED LINKS</span></span>

[<span data-ttu-id="a7123-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="a7123-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


