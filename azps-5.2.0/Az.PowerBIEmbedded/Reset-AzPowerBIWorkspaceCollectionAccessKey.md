---
external help file: Microsoft.Azure.PowerShell.Cmdlets.PowerBIEmbedded.dll-Help.xml
Module Name: Az.PowerBIEmbedded
ms.assetid: 8FB2D9A0-BF7A-482D-B3A2-566FCA8C62A1
online version: https://docs.microsoft.com/en-us/powershell/module/az.powerbiembedded/reset-azpowerbiworkspacecollectionaccesskey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/PowerBIEmbedded/PowerBIEmbedded/help/Reset-AzPowerBIWorkspaceCollectionAccessKey.md
ms.openlocfilehash: d9e30c81eb0e2422b91be79bcfc7c732291c30cb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98301440"
---
# <span data-ttu-id="366ef-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="366ef-101">Reset-AzPowerBIWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="366ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="366ef-102">SYNOPSIS</span></span>
<span data-ttu-id="366ef-103">Setzt die angegebene Zugriffstaste zurück.</span><span class="sxs-lookup"><span data-stu-id="366ef-103">Resets the specified access key.</span></span>

## <span data-ttu-id="366ef-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="366ef-104">SYNTAX</span></span>

```
Reset-AzPowerBIWorkspaceCollectionAccessKey [-ResourceGroupName] <String> [-WorkspaceCollectionName] <String>
 [-Key1] [-Key2] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="366ef-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="366ef-105">DESCRIPTION</span></span>
<span data-ttu-id="366ef-106">Das **Cmdlet "Reset-AzPowerBIWorkspaceCollectionAccessKey"** setzt die angegebene Zugriffstaste in Ihrer Power BI-Arbeitsbereichssammlung zurück.</span><span class="sxs-lookup"><span data-stu-id="366ef-106">The **Reset-AzPowerBIWorkspaceCollectionAccessKey** cmdlet resets the specified access key in your Power BI workspace collection.</span></span>

## <span data-ttu-id="366ef-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="366ef-107">EXAMPLES</span></span>

### <span data-ttu-id="366ef-108">Beispiel 1: Zurücksetzen des primären Zugriffsschlüssels</span><span class="sxs-lookup"><span data-stu-id="366ef-108">Example 1: Reset the primary access key</span></span>
```
PS C:\>Reset-AzPowerBIWorkspaceCollectionAccessKey -ResourceGroupName "ResourceGroup17" -WorkspaceCollectionName "WCN11" -Key1
```

<span data-ttu-id="366ef-109">Mit diesem Befehl wird der primäre Zugriffsschlüssel für die Arbeitsbereichssammlung mit dem Namen WCN11 in der angegebenen Ressourcengruppe zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="366ef-109">This command resets the primary access key for the workspace collection named WCN11 in the specified resource group.</span></span>

## <span data-ttu-id="366ef-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="366ef-110">PARAMETERS</span></span>

### <span data-ttu-id="366ef-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="366ef-111">-DefaultProfile</span></span>
<span data-ttu-id="366ef-112">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="366ef-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="366ef-113">-Key1</span><span class="sxs-lookup"><span data-stu-id="366ef-113">-Key1</span></span>
<span data-ttu-id="366ef-114">Gibt an, dass mit diesem Cmdlet der primäre Zugriffsschlüssel zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="366ef-114">Indicates that this cmdlet resets the primary access key.</span></span>

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

### <span data-ttu-id="366ef-115">-Key2</span><span class="sxs-lookup"><span data-stu-id="366ef-115">-Key2</span></span>
<span data-ttu-id="366ef-116">Gibt an, dass mit diesem Cmdlet die sekundäre Zugriffstaste zurückgesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="366ef-116">Indicates that this cmdlet resets the secondary access key.</span></span>

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

### <span data-ttu-id="366ef-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="366ef-117">-ResourceGroupName</span></span>
<span data-ttu-id="366ef-118">Gibt den Namen der Ressourcengruppe der Sammlung an.</span><span class="sxs-lookup"><span data-stu-id="366ef-118">Specifies the name of the resource group of the collection.</span></span>

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

### <span data-ttu-id="366ef-119">-WorkspaceCollectionName</span><span class="sxs-lookup"><span data-stu-id="366ef-119">-WorkspaceCollectionName</span></span>
<span data-ttu-id="366ef-120">Gibt den Namen der Power BI-Arbeitsbereichssammlung an, für die dieses Cmdlet verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="366ef-120">Specifies the name of the Power BI workspace collection on which this cmdlet operates.</span></span>

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

### <span data-ttu-id="366ef-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="366ef-121">-Confirm</span></span>
<span data-ttu-id="366ef-122">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="366ef-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="366ef-123">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="366ef-123">-WhatIf</span></span>
<span data-ttu-id="366ef-124">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="366ef-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="366ef-125">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="366ef-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="366ef-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="366ef-126">CommonParameters</span></span>
<span data-ttu-id="366ef-127">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="366ef-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="366ef-128">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="366ef-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="366ef-129">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="366ef-129">INPUTS</span></span>

### <span data-ttu-id="366ef-130">System.String</span><span class="sxs-lookup"><span data-stu-id="366ef-130">System.String</span></span>

## <span data-ttu-id="366ef-131">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="366ef-131">OUTPUTS</span></span>

### <span data-ttu-id="366ef-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="366ef-132">Microsoft.Azure.Commands.Management.PowerBIEmbedded.Models.PSWorkspaceCollectionAccessKey</span></span>

## <span data-ttu-id="366ef-133">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="366ef-133">NOTES</span></span>

## <span data-ttu-id="366ef-134">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="366ef-134">RELATED LINKS</span></span>

[<span data-ttu-id="366ef-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span><span class="sxs-lookup"><span data-stu-id="366ef-135">Get-AzPowerBIWorkspaceCollectionAccessKey</span></span>](./Get-AzPowerBIWorkspaceCollectionAccessKey.md)


