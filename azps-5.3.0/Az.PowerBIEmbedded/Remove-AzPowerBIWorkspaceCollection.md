---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 2D63CC6D-AB02-4299-A922-4057D6F595D7
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/remove-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Remove-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: c8e6f54b5bd4deeb4ef24559298306880740c6d3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98459771"
---
# <span data-ttu-id="21ac1-101">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="21ac1-101">Remove-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="21ac1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21ac1-102">SYNOPSIS</span></span>
<span data-ttu-id="21ac1-103">Entfernt eine Power BI-Arbeitsbereichssammlung.</span><span class="sxs-lookup"><span data-stu-id="21ac1-103">Removes a Power BI workspace collection.</span></span>

## <span data-ttu-id="21ac1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="21ac1-104">SYNTAX</span></span>

```
Remove-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="21ac1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="21ac1-105">DESCRIPTION</span></span>
<span data-ttu-id="21ac1-106">Das **Cmdlet "Remove-AzPowerBIWorkspaceCollection"** entfernt eine Power BI-Arbeitsbereichssammlung aus Ihrem Azure-Abonnement und der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="21ac1-106">The **Remove-AzPowerBIWorkspaceCollection** cmdlet removes a Power BI workspace collection from your Azure subscription and resource group.</span></span>

## <span data-ttu-id="21ac1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="21ac1-107">EXAMPLES</span></span>

### <span data-ttu-id="21ac1-108">Beispiel 1: Entfernen einer Arbeitsbereichssammlung</span><span class="sxs-lookup"><span data-stu-id="21ac1-108">Example 1: Remove a workspace collection</span></span>
```
PS C:\>Remove-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11"
```

<span data-ttu-id="21ac1-109">Mit diesem Befehl wird die Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe entfernt.</span><span class="sxs-lookup"><span data-stu-id="21ac1-109">This command removes the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="21ac1-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="21ac1-110">PARAMETERS</span></span>

### <span data-ttu-id="21ac1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21ac1-111">-DefaultProfile</span></span>
<span data-ttu-id="21ac1-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="21ac1-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="21ac1-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="21ac1-113">-ResourceGroupName</span></span>
<span data-ttu-id="21ac1-114">Gibt den Namen der Ressourcengruppe an, aus der mit diesem Cmdlet eine Arbeitsbereichssammlung entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="21ac1-114">Specifies the name of the resource group from which this cmdlet removes a workspace collection.</span></span>

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

### <span data-ttu-id="21ac1-115">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="21ac1-115">-WorkspaceCollectionName</span></span>
<span data-ttu-id="21ac1-116">Gibt den Namen der Power BI-Arbeitsbereichssammlung an, die von diesem Cmdlet entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="21ac1-116">Specifies the name of the Power BI workspace collection that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="21ac1-117">-Confirm</span><span class="sxs-lookup"><span data-stu-id="21ac1-117">-Confirm</span></span>
<span data-ttu-id="21ac1-118">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="21ac1-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="21ac1-119">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="21ac1-119">-WhatIf</span></span>
<span data-ttu-id="21ac1-120">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="21ac1-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21ac1-121">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="21ac1-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="21ac1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="21ac1-122">CommonParameters</span></span>
<span data-ttu-id="21ac1-123">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="21ac1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="21ac1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="21ac1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="21ac1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="21ac1-125">INPUTS</span></span>

### <span data-ttu-id="21ac1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="21ac1-126">System.String</span></span>

## <span data-ttu-id="21ac1-127">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="21ac1-127">OUTPUTS</span></span>

### <span data-ttu-id="21ac1-128">System.Void</span><span class="sxs-lookup"><span data-stu-id="21ac1-128">System.Void</span></span>

## <span data-ttu-id="21ac1-129">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="21ac1-129">NOTES</span></span>

## <span data-ttu-id="21ac1-130">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="21ac1-130">RELATED LINKS</span></span>

[<span data-ttu-id="21ac1-131">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="21ac1-131">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="21ac1-132">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="21ac1-132">New-AzPowerBIWorkspaceCollection</span></span>](./New-AzPowerBIWorkspaceCollection.md)


