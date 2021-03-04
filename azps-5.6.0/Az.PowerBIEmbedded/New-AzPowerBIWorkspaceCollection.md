---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 9F9E4273-6747-4963-AF1F-C0AEB46770A4
online version: https://docs.microsoft.com/powershell/module/az.powerbiembedded/new-azpowerbiworkspacecollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/New-AzPowerBIWorkspaceCollection.md
ms.openlocfilehash: 69f90f84d7e142ea3471c7e6871baac145f1b9c0
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929880"
---
# <span data-ttu-id="a5b00-101">New-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a5b00-101">New-AzPowerBIWorkspaceCollection</span></span>

## <span data-ttu-id="a5b00-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5b00-102">SYNOPSIS</span></span>
<span data-ttu-id="a5b00-103">Erstellt eine Power BI-Arbeitsbereichssammlung.</span><span class="sxs-lookup"><span data-stu-id="a5b00-103">Creates a Power BI workspace collection.</span></span>

## <span data-ttu-id="a5b00-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="a5b00-104">SYNTAX</span></span>

```
New-AzPowerBIWorkspaceCollection [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Location] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5b00-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="a5b00-105">DESCRIPTION</span></span>
<span data-ttu-id="a5b00-106">Das **Cmdlet New-AzPowerBIWorkspaceCollection** erstellt eine Power BI-Arbeitsbereichssammlung für Ihr Azure-Abonnement in der angegebenen Ressourcengruppe und dem angegebenen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="a5b00-106">The **New-AzPowerBIWorkspaceCollection** cmdlet creates a Power BI workspace collection for your Azure subscription in the specified resource group and location.</span></span>

## <span data-ttu-id="a5b00-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="a5b00-107">EXAMPLES</span></span>

### <span data-ttu-id="a5b00-108">Beispiel 1: Erstellen einer Arbeitsbereichssammlung</span><span class="sxs-lookup"><span data-stu-id="a5b00-108">Example 1: Create a workspace collection</span></span>
```
PS C:\>New-AzPowerBIWorkspaceCollection -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Location "Japan West"
```

<span data-ttu-id="a5b00-109">Mit diesem Befehl wird eine Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe am angegebenen Speicherort erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5b00-109">This command creates a workspace collection named WCN11 in the specified resource group in the specified location.</span></span>

## <span data-ttu-id="a5b00-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="a5b00-110">PARAMETERS</span></span>

### <span data-ttu-id="a5b00-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5b00-111">-DefaultProfile</span></span>
<span data-ttu-id="a5b00-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="a5b00-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5b00-113">-Location</span><span class="sxs-lookup"><span data-stu-id="a5b00-113">-Location</span></span>
<span data-ttu-id="a5b00-114">Gibt den Azure-Speicherort an, an dem dieses Cmdlet eine Arbeitsbereichssammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5b00-114">Specifies the Azure location in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a5b00-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5b00-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5b00-116">Gibt den Namen der Ressourcengruppe an, in der dieses Cmdlet eine Arbeitsbereichssammlung erstellt.</span><span class="sxs-lookup"><span data-stu-id="a5b00-116">Specifies the name of the resource group in which this cmdlet creates a workspace collection.</span></span>

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

### <span data-ttu-id="a5b00-117">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="a5b00-117">-WorkspaceCollectionName</span></span>
<span data-ttu-id="a5b00-118">Gibt einen Namen für die Power BI-Arbeitsbereichssammlung an.</span><span class="sxs-lookup"><span data-stu-id="a5b00-118">Specifies a name for the Power BI workspace collection.</span></span>

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

### <span data-ttu-id="a5b00-119">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="a5b00-119">-Confirm</span></span>
<span data-ttu-id="a5b00-120">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="a5b00-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5b00-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5b00-121">-WhatIf</span></span>
<span data-ttu-id="a5b00-122">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a5b00-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5b00-123">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a5b00-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5b00-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5b00-124">CommonParameters</span></span>
<span data-ttu-id="a5b00-125">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5b00-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5b00-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5b00-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5b00-127">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="a5b00-127">INPUTS</span></span>

### <span data-ttu-id="a5b00-128">System.String</span><span class="sxs-lookup"><span data-stu-id="a5b00-128">System.String</span></span>

## <span data-ttu-id="a5b00-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="a5b00-129">OUTPUTS</span></span>

### <span data-ttu-id="a5b00-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a5b00-130">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollection</span></span>

## <span data-ttu-id="a5b00-131">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="a5b00-131">NOTES</span></span>

## <span data-ttu-id="a5b00-132">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="a5b00-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5b00-133">Get-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a5b00-133">Get-AzPowerBIWorkspaceCollection</span></span>](./Get-AzPowerBIWorkspaceCollection.md)

[<span data-ttu-id="a5b00-134">Remove-AzPowerBIWorkspaceCollection</span><span class="sxs-lookup"><span data-stu-id="a5b00-134">Remove-AzPowerBIWorkspaceCollection</span></span>](./Remove-AzPowerBIWorkspaceCollection.md)


