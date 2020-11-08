---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/restore-azoperationalinsightsworkspace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Restore-AzOperationalInsightsWorkspace.md
ms.openlocfilehash: 01354106e3d6ad9fbe33c97f6bcd774c62be7ccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176131"
---
# <span data-ttu-id="dbc57-101">Restore-AzOperationalInsightsWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbc57-101">Restore-AzOperationalInsightsWorkspace</span></span>

## <span data-ttu-id="dbc57-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="dbc57-102">SYNOPSIS</span></span>
<span data-ttu-id="dbc57-103">Wiederherstellen eines gelöschten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="dbc57-103">Restore a deleted workspace.</span></span>

## <span data-ttu-id="dbc57-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="dbc57-104">SYNTAX</span></span>

```
Restore-AzOperationalInsightsWorkspace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dbc57-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dbc57-105">DESCRIPTION</span></span>
<span data-ttu-id="dbc57-106">Wiederherstellen eines gelöschten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="dbc57-106">Restore a deleted workspace.</span></span>

## <span data-ttu-id="dbc57-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="dbc57-107">EXAMPLES</span></span>

### <span data-ttu-id="dbc57-108">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dbc57-108">Example 1</span></span>
```powershell
PS C:\> $workspace = New-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
PS C:\> $workspace | Remove-AzOperationalInsightsWorkspace
PS C:\> $workspace = Restore-AzOperationalInsightsWorkspace -ResourceGroupName $rgname -Name $wsname -Location $wslocation
```

<span data-ttu-id="dbc57-109">Wiederherstellen eines gelöschten Arbeitsbereichs</span><span class="sxs-lookup"><span data-stu-id="dbc57-109">Restore deleted workspace.</span></span>

## <span data-ttu-id="dbc57-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="dbc57-110">PARAMETERS</span></span>

### <span data-ttu-id="dbc57-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbc57-111">-DefaultProfile</span></span>
<span data-ttu-id="dbc57-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="dbc57-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dbc57-113">-Force</span><span class="sxs-lookup"><span data-stu-id="dbc57-113">-Force</span></span>
<span data-ttu-id="dbc57-114">Keine Bestätigung anfordern.</span><span class="sxs-lookup"><span data-stu-id="dbc57-114">Don't ask for confirmation.</span></span>

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

### <span data-ttu-id="dbc57-115">-Standort</span><span class="sxs-lookup"><span data-stu-id="dbc57-115">-Location</span></span>
<span data-ttu-id="dbc57-116">Die geografische Region, in der der Arbeitsbereich erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc57-116">The geographic region that the workspace will be created in.</span></span>

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

### <span data-ttu-id="dbc57-117">-Name</span><span class="sxs-lookup"><span data-stu-id="dbc57-117">-Name</span></span>
<span data-ttu-id="dbc57-118">Der Arbeitsbereichsname.</span><span class="sxs-lookup"><span data-stu-id="dbc57-118">The workspace name.</span></span>

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

### <span data-ttu-id="dbc57-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dbc57-119">-ResourceGroupName</span></span>
<span data-ttu-id="dbc57-120">Der Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="dbc57-120">The resource group name.</span></span>

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

### <span data-ttu-id="dbc57-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dbc57-121">-Confirm</span></span>
<span data-ttu-id="dbc57-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dbc57-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dbc57-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dbc57-123">-WhatIf</span></span>
<span data-ttu-id="dbc57-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dbc57-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dbc57-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dbc57-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dbc57-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbc57-126">CommonParameters</span></span>
<span data-ttu-id="dbc57-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dbc57-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbc57-128">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="dbc57-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbc57-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="dbc57-129">INPUTS</span></span>

### <span data-ttu-id="dbc57-130">System. String</span><span class="sxs-lookup"><span data-stu-id="dbc57-130">System.String</span></span>

## <span data-ttu-id="dbc57-131">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="dbc57-131">OUTPUTS</span></span>

### <span data-ttu-id="dbc57-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="dbc57-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

## <span data-ttu-id="dbc57-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="dbc57-133">NOTES</span></span>

## <span data-ttu-id="dbc57-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="dbc57-134">RELATED LINKS</span></span>
