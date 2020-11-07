---
external help file: Microsoft.Azure.Commands.OperationalInsights.dll-Help.xml
Module Name: AzureRM.OperationalInsights
ms.assetid: 5C1C51FE-747F-4176-84ED-A28AA3475581
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.operationalinsights/remove-azurermoperationalinsightsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/OperationalInsights/Commands.OperationalInsights/help/Remove-AzureRmOperationalInsightsDataSource.md
ms.openlocfilehash: a3f650861f70ad9110f4716e5034cd5e7f930343
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664367"
---
# <span data-ttu-id="bad76-101">Remove-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bad76-101">Remove-AzureRmOperationalInsightsDataSource</span></span>

## <span data-ttu-id="bad76-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="bad76-102">SYNOPSIS</span></span>
<span data-ttu-id="bad76-103">Löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="bad76-103">Deletes a data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bad76-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="bad76-104">SYNTAX</span></span>

### <span data-ttu-id="bad76-105">ByWorkspaceName (Standard)</span><span class="sxs-lookup"><span data-stu-id="bad76-105">ByWorkspaceName (Default)</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-ResourceGroupName] <String> [-WorkspaceName] <String>
 [-Name] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bad76-106">ByWorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="bad76-106">ByWorkspaceObject</span></span>
```
Remove-AzureRmOperationalInsightsDataSource [-Workspace] <PSWorkspace> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bad76-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bad76-107">DESCRIPTION</span></span>
<span data-ttu-id="bad76-108">Das Cmdlet **Remove-AzureRmOperationalInsightsDataSource** löscht eine Datenquelle.</span><span class="sxs-lookup"><span data-stu-id="bad76-108">The **Remove-AzureRmOperationalInsightsDataSource** cmdlet deletes a data source.</span></span>

## <span data-ttu-id="bad76-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="bad76-109">EXAMPLES</span></span>

## <span data-ttu-id="bad76-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="bad76-110">PARAMETERS</span></span>

### <span data-ttu-id="bad76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bad76-111">-DefaultProfile</span></span>
<span data-ttu-id="bad76-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="bad76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bad76-113">-Force</span><span class="sxs-lookup"><span data-stu-id="bad76-113">-Force</span></span>
<span data-ttu-id="bad76-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="bad76-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bad76-115">-Name</span><span class="sxs-lookup"><span data-stu-id="bad76-115">-Name</span></span>
<span data-ttu-id="bad76-116">Gibt den Namen einer Datenquelle an, die gelöscht werden soll.</span><span class="sxs-lookup"><span data-stu-id="bad76-116">Specifies the name of a data source to delete.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad76-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bad76-117">-ResourceGroupName</span></span>
<span data-ttu-id="bad76-118">Gibt den Namen einer Ressourcengruppe an, die Computer enthält.</span><span class="sxs-lookup"><span data-stu-id="bad76-118">Specifies the name of a resource group that contains computers.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad76-119">– Arbeitsbereich</span><span class="sxs-lookup"><span data-stu-id="bad76-119">-Workspace</span></span>
<span data-ttu-id="bad76-120">Gibt einen Arbeitsbereich an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bad76-120">Specifies a workspace in which this cmdlet operates.</span></span>

```yaml
Type: PSWorkspace
Parameter Sets: ByWorkspaceObject
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bad76-121">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="bad76-121">-WorkspaceName</span></span>
<span data-ttu-id="bad76-122">Gibt den Namen eines Arbeitsbereichs an, in dem dieses Cmdlet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="bad76-122">Specifies the name of a workspace in which this cmdlet operates.</span></span>

```yaml
Type: String
Parameter Sets: ByWorkspaceName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bad76-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="bad76-123">-Confirm</span></span>
<span data-ttu-id="bad76-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="bad76-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bad76-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bad76-125">-WhatIf</span></span>
<span data-ttu-id="bad76-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bad76-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bad76-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="bad76-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bad76-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bad76-128">CommonParameters</span></span>
<span data-ttu-id="bad76-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bad76-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bad76-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bad76-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bad76-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="bad76-131">INPUTS</span></span>

### <span data-ttu-id="bad76-132">PSWorkspace</span><span class="sxs-lookup"><span data-stu-id="bad76-132">PSWorkspace</span></span>
<span data-ttu-id="bad76-133">Der Parameter "Workspace" akzeptiert den Wert vom Typ "PSWorkspace" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="bad76-133">Parameter 'Workspace' accepts value of type 'PSWorkspace' from the pipeline</span></span>

## <span data-ttu-id="bad76-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="bad76-134">OUTPUTS</span></span>

## <span data-ttu-id="bad76-135">Notizen</span><span class="sxs-lookup"><span data-stu-id="bad76-135">NOTES</span></span>
* <span data-ttu-id="bad76-136">Schlüsselwörter: Azure, azurerm, arm, Resource, Management, Manager, Operational, Insights</span><span class="sxs-lookup"><span data-stu-id="bad76-136">Keywords: azure, azurerm, arm, resource, management, manager, operational, insights</span></span>

## <span data-ttu-id="bad76-137">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="bad76-137">RELATED LINKS</span></span>

[<span data-ttu-id="bad76-138">Get-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bad76-138">Get-AzureRmOperationalInsightsDataSource</span></span>](./Get-AzureRmOperationalInsightsDataSource.md)

[<span data-ttu-id="bad76-139">Satz-AzureRmOperationalInsightsDataSource</span><span class="sxs-lookup"><span data-stu-id="bad76-139">Set-AzureRmOperationalInsightsDataSource</span></span>](./Set-AzureRmOperationalInsightsDataSource.md)


