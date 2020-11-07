---
external help file: Microsoft.Azure.PowerShell.Cmdlets.OperationalInsights.dll-Help.xml
Module Name: Az.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/az.operationalinsights/remove-azoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/OperationalInsights/OperationalInsights/help/Remove-AzOperationalInsightsDataSource.md
ms.openlocfilehash: d8ec5eed1b6c955720822e28bf54da68e9aefcac
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93824072"
---
# <span data-ttu-id="7c6d0-101">Remove-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7c6d0-101">Remove-AzOperationalInsightsDataSource</span></span>

## <span data-ttu-id="7c6d0-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7c6d0-102">SYNOPSIS</span></span>
<span data-ttu-id="7c6d0-103">Löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-103">Deletes a data source.</span></span>

## <span data-ttu-id="7c6d0-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7c6d0-104">SYNTAX</span></span>

### <span data-ttu-id="7c6d0-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7c6d0-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String> [-Name] <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7c6d0-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="7c6d0-106">ByWorkspaceObject</span></span>
```
Remove-AzOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7c6d0-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7c6d0-107">DESCRIPTION</span></span>
<span data-ttu-id="7c6d0-108">Das Cmdlet **Remove-AzOperationalInsightsDataSource** löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-108">The **Remove-AzOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="7c6d0-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7c6d0-109">EXAMPLES</span></span>

## <span data-ttu-id="7c6d0-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="7c6d0-110">PARAMETERS</span></span>

### <span data-ttu-id="7c6d0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c6d0-111">-DefaultProfile</span></span>
<span data-ttu-id="7c6d0-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7c6d0-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7c6d0-113">-Force</span><span class="sxs-lookup"><span data-stu-id="7c6d0-113">-Force</span></span>
<span data-ttu-id="7c6d0-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7c6d0-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7c6d0-115">-Name</span></span>
<span data-ttu-id="7c6d0-116">Gibt den Namen einer Datenquelle an, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6d0-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c6d0-117">-ResourceGroupName</span></span>
<span data-ttu-id="7c6d0-118">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6d0-119">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="7c6d0-119">-Workspace</span></span>
<span data-ttu-id="7c6d0-120">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6d0-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="7c6d0-121">-WorkspaceName</span></span>
<span data-ttu-id="7c6d0-122">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: System.String
Parameter Sets: ByWorkspaceName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c6d0-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7c6d0-123">-Confirm</span></span>
<span data-ttu-id="7c6d0-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7c6d0-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7c6d0-125">-WhatIf</span></span>
<span data-ttu-id="7c6d0-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7c6d0-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7c6d0-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c6d0-128">CommonParameters</span></span>
<span data-ttu-id="7c6d0-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7c6d0-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c6d0-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c6d0-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c6d0-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7c6d0-131">INPUTS</span></span>

### <span data-ttu-id="7c6d0-132">Microsoft. Azure. Commands. OperationalInsights. Models. PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="7c6d0-132">Microsoft.Azure.Commands.OperationalInsights.Models.PSWorkspace</span></span>

### <span data-ttu-id="7c6d0-133">System. String</span><span class="sxs-lookup"><span data-stu-id="7c6d0-133">System.String</span></span>

## <span data-ttu-id="7c6d0-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7c6d0-134">OUTPUTS</span></span>

### <span data-ttu-id="7c6d0-135">System. void</span><span class="sxs-lookup"><span data-stu-id="7c6d0-135">System.Void</span></span>

## <span data-ttu-id="7c6d0-136">Notizen</span><span class="sxs-lookup"><span data-stu-id="7c6d0-136">NOTES</span></span>
* <span data-ttu-id="7c6d0-137">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="7c6d0-137">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="7c6d0-138">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7c6d0-138">RELATED LINKS</span></span>

[<span data-ttu-id="7c6d0-139">Get-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7c6d0-139">Get-AzOperationalInsightsDataSource</span></span>](./Get-AzOperationalInsightsDataSource.md)

[<span data-ttu-id="7c6d0-140">Satz-AzOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="7c6d0-140">Set-AzOperationalInsightsDataSource</span></span>](./Set-AzOperationalInsightsDataSource.md)


