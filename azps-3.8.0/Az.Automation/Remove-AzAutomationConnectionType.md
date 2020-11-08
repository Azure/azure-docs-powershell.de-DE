---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 92B69069-0F98-428A-B05C-BBA09EBC0381
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/remove-azautomationconnectiontype
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Remove-AzAutomationConnectionType.md
ms.openlocfilehash: 5eb31abcc632f06402b4196be8be4c5e32cdacf0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "94005143"
---
# <span data-ttu-id="dfc79-101">Remove-AzAutomationConnectionType</span><span class="sxs-lookup"><span data-stu-id="dfc79-101">Remove-AzAutomationConnectionType</span></span>

## <span data-ttu-id="dfc79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dfc79-102">SYNOPSIS</span></span>
<span data-ttu-id="dfc79-103">Entfernt einen Automatisierungs Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="dfc79-103">Removes an Automation connection type.</span></span>

## <span data-ttu-id="dfc79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dfc79-104">SYNTAX</span></span>

```
Remove-AzAutomationConnectionType [-Name] <String> [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dfc79-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dfc79-105">DESCRIPTION</span></span>
<span data-ttu-id="dfc79-106">Das Cmdlet **Remove-AzAutomationConnectionType** entfernt einen Verbindungstyp aus Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dfc79-106">The **Remove-AzAutomationConnectionType** cmdlet removes a connection type from Azure Automation.</span></span>
<span data-ttu-id="dfc79-107">Alle Verbindungen, die dem von Ihnen gelöschten Verbindungstyp zugeordnet sind, werden unbrauchbar.</span><span class="sxs-lookup"><span data-stu-id="dfc79-107">All connections that are associated with the connection type that you delete become unusable.</span></span>
<span data-ttu-id="dfc79-108">Entfernen Sie Sie, es sei denn, Sie erstellen einen neuen Verbindungstyp, der die folgenden Kriterien erfüllt:</span><span class="sxs-lookup"><span data-stu-id="dfc79-108">Remove them, unless you create a new connection type that meets the following criteria:</span></span> 
- <span data-ttu-id="dfc79-109">Der Typ hat denselben Namen wie der ursprüngliche Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="dfc79-109">The type has the same name as the original connection type.</span></span> 
- <span data-ttu-id="dfc79-110">Der Typ hat die gleichen Felddefinitionen wie der ursprüngliche Verbindungstyp.</span><span class="sxs-lookup"><span data-stu-id="dfc79-110">The type has the same field definitions as the original connection type.</span></span>
<span data-ttu-id="dfc79-111">Es können zusätzliche Felder vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dfc79-111">It can have additional fields.</span></span>

## <span data-ttu-id="dfc79-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dfc79-112">EXAMPLES</span></span>

### <span data-ttu-id="dfc79-113">Beispiel 1: Entfernen eines Verbindungstyps</span><span class="sxs-lookup"><span data-stu-id="dfc79-113">Example 1: Remove a connection type</span></span>
```
PS C:\>Remove-AzAutomationConnectionType -AutomationAccountName "Contoso17" -Name "ContosoConnectionType" -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dfc79-114">Dieser Befehl entfernt einen Verbindungstyp mit dem Namen ContosoConnectionType im Automatisierungs Konto mit dem Namen Contoso17.</span><span class="sxs-lookup"><span data-stu-id="dfc79-114">This command removes a connection type named ContosoConnectionType in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="dfc79-115">Parameter</span><span class="sxs-lookup"><span data-stu-id="dfc79-115">PARAMETERS</span></span>

### <span data-ttu-id="dfc79-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dfc79-116">-AutomationAccountName</span></span>
<span data-ttu-id="dfc79-117">Gibt den Namen des Automatisierungs Kontos an, für das dieses Cmdlet einen Verbindungstyp entfernt.</span><span class="sxs-lookup"><span data-stu-id="dfc79-117">Specifies the name of the Automation account for which this cmdlet removes a connection type.</span></span>

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

### <span data-ttu-id="dfc79-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfc79-118">-DefaultProfile</span></span>
<span data-ttu-id="dfc79-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="dfc79-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dfc79-120">-Force</span><span class="sxs-lookup"><span data-stu-id="dfc79-120">-Force</span></span>
<span data-ttu-id="dfc79-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="dfc79-121">ps_force</span></span>

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

### <span data-ttu-id="dfc79-122">-Name</span><span class="sxs-lookup"><span data-stu-id="dfc79-122">-Name</span></span>
<span data-ttu-id="dfc79-123">Gibt den Namen des Automatisierungs Verbindungstyps an, den dieses Cmdlet entfernt.</span><span class="sxs-lookup"><span data-stu-id="dfc79-123">Specifies the name of the Automation connection type that this cmdlet removes.</span></span>

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

### <span data-ttu-id="dfc79-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dfc79-124">-ResourceGroupName</span></span>
<span data-ttu-id="dfc79-125">Gibt den Namen der Ressourcengruppe an, aus der mit diesem Cmdlet ein Automatisierungs Verbindungstyp entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc79-125">Specifies the name of the resource group from which this cmdlet removes an Automation connection type.</span></span>

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

### <span data-ttu-id="dfc79-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dfc79-126">-Confirm</span></span>
<span data-ttu-id="dfc79-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dfc79-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dfc79-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dfc79-128">-WhatIf</span></span>
<span data-ttu-id="dfc79-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dfc79-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dfc79-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dfc79-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dfc79-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfc79-131">CommonParameters</span></span>
<span data-ttu-id="dfc79-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfc79-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfc79-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfc79-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfc79-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dfc79-134">INPUTS</span></span>

### <span data-ttu-id="dfc79-135">System. String</span><span class="sxs-lookup"><span data-stu-id="dfc79-135">System.String</span></span>

## <span data-ttu-id="dfc79-136">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dfc79-136">OUTPUTS</span></span>

### <span data-ttu-id="dfc79-137">System. void</span><span class="sxs-lookup"><span data-stu-id="dfc79-137">System.Void</span></span>

## <span data-ttu-id="dfc79-138">Notizen</span><span class="sxs-lookup"><span data-stu-id="dfc79-138">NOTES</span></span>

## <span data-ttu-id="dfc79-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dfc79-139">RELATED LINKS</span></span>

[<span data-ttu-id="dfc79-140">Remove-AzAutomationConnection</span><span class="sxs-lookup"><span data-stu-id="dfc79-140">Remove-AzAutomationConnection</span></span>](./Remove-AzAutomationConnection.md)


