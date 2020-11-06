---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: 49674f372e477ee7050a6ccf7d833aaee59bac3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481725"
---
# <span data-ttu-id="92df5-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="92df5-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="92df5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92df5-102">SYNOPSIS</span></span>
<span data-ttu-id="92df5-103">Löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="92df5-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92df5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92df5-104">SYNTAX</span></span>

### <span data-ttu-id="92df5-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="92df5-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92df5-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="92df5-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="92df5-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92df5-107">DESCRIPTION</span></span>
<span data-ttu-id="92df5-108">Das Cmdlet **Remove-AzureRmOperationalInsightsDataSource** löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="92df5-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="92df5-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92df5-109">EXAMPLES</span></span>

## <span data-ttu-id="92df5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="92df5-110">PARAMETERS</span></span>

### <span data-ttu-id="92df5-111">-Force</span><span class="sxs-lookup"><span data-stu-id="92df5-111">-Force</span></span>
<span data-ttu-id="92df5-112">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="92df5-112">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="92df5-113">-Name</span><span class="sxs-lookup"><span data-stu-id="92df5-113">-Name</span></span>
<span data-ttu-id="92df5-114">Gibt den Namen einer Datenquelle an, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="92df5-114">Specifies the name of a data source to delete.</span></span>

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

### <span data-ttu-id="92df5-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92df5-115">-ResourceGroupName</span></span>
<span data-ttu-id="92df5-116">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="92df5-116">Specifies the name of a resource group that contains computers.</span></span>

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

### <span data-ttu-id="92df5-117">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="92df5-117">-Workspace</span></span>
<span data-ttu-id="92df5-118">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="92df5-118">Specifies a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="92df5-119">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="92df5-119">-WorkspaceName</span></span>
<span data-ttu-id="92df5-120">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="92df5-120">Specifies the name of a workspace in which this cmdlet operates.</span></span>

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

### <span data-ttu-id="92df5-121">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92df5-121">-Confirm</span></span>
<span data-ttu-id="92df5-122">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92df5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92df5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92df5-123">-WhatIf</span></span>
<span data-ttu-id="92df5-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92df5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="92df5-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92df5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92df5-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92df5-126">-DefaultProfile</span></span>
<span data-ttu-id="92df5-127">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92df5-127">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92df5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92df5-128">CommonParameters</span></span>
<span data-ttu-id="92df5-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92df5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92df5-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92df5-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92df5-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92df5-131">INPUTS</span></span>

### <span data-ttu-id="92df5-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="92df5-132">PSWorkspace</span></span>
<span data-ttu-id="92df5-133">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="92df5-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="92df5-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92df5-134">OUTPUTS</span></span>

## <span data-ttu-id="92df5-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="92df5-135">NOTES</span></span>
* <span data-ttu-id="92df5-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="92df5-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="92df5-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92df5-137">RELATED LINKS</span></span>

[<span data-ttu-id="92df5-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="92df5-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="92df5-139">Satz-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="92df5-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


