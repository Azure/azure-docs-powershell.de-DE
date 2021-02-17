---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: b1c77b2a00f460e6d05483037a46e5472a25d266
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100403033"
---
# <span data-ttu-id="9d452-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9d452-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="9d452-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9d452-102">SYNOPSIS</span></span>
<span data-ttu-id="9d452-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9d452-103">Removes an action group.</span></span>

## <span data-ttu-id="9d452-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9d452-104">SYNTAX</span></span>

### <span data-ttu-id="9d452-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9d452-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9d452-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9d452-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9d452-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9d452-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9d452-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9d452-108">DESCRIPTION</span></span>
<span data-ttu-id="9d452-109">Das **Cmdlet "Remove-AzActionGroup"** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9d452-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="9d452-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9d452-110">EXAMPLES</span></span>

### <span data-ttu-id="9d452-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="9d452-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="9d452-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9d452-112">PARAMETERS</span></span>

### <span data-ttu-id="9d452-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9d452-113">-DefaultProfile</span></span>
<span data-ttu-id="9d452-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9d452-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9d452-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9d452-115">-InputObject</span></span>
<span data-ttu-id="9d452-116">Die Aktionsgruppe "resourc"</span><span class="sxs-lookup"><span data-stu-id="9d452-116">The action group resourc</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9d452-117">-Name</span><span class="sxs-lookup"><span data-stu-id="9d452-117">-Name</span></span>
<span data-ttu-id="9d452-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9d452-118">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d452-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9d452-119">-ResourceGroupName</span></span>
<span data-ttu-id="9d452-120">Die Ressourcengruppe nam</span><span class="sxs-lookup"><span data-stu-id="9d452-120">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d452-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9d452-121">-ResourceId</span></span>
<span data-ttu-id="9d452-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="9d452-122">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9d452-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9d452-123">-Confirm</span></span>
<span data-ttu-id="9d452-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9d452-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9d452-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9d452-125">-WhatIf</span></span>
<span data-ttu-id="9d452-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9d452-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9d452-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9d452-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9d452-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9d452-128">CommonParameters</span></span>
<span data-ttu-id="9d452-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9d452-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9d452-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9d452-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9d452-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9d452-131">INPUTS</span></span>

### <span data-ttu-id="9d452-132">System.String</span><span class="sxs-lookup"><span data-stu-id="9d452-132">System.String</span></span>

### <span data-ttu-id="9d452-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9d452-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9d452-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9d452-134">OUTPUTS</span></span>

### <span data-ttu-id="9d452-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9d452-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9d452-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9d452-136">NOTES</span></span>

## <span data-ttu-id="9d452-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9d452-137">RELATED LINKS</span></span>

<span data-ttu-id="9d452-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="9d452-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)</span></span>

