---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 8D8FE2FE-03E7-453E-B968-E28B07E42EF2
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActionGroup.md
ms.openlocfilehash: ebe0ecd51b59c6ff28fc0b5655a9b8ba6b8b4ee6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100147348"
---
# <span data-ttu-id="238d2-101">Remove-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="238d2-101">Remove-AzActionGroup</span></span>

## <span data-ttu-id="238d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="238d2-102">SYNOPSIS</span></span>
<span data-ttu-id="238d2-103">Entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="238d2-103">Removes an action group.</span></span>

## <span data-ttu-id="238d2-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="238d2-104">SYNTAX</span></span>

### <span data-ttu-id="238d2-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="238d2-105">ByPropertyName (Default)</span></span>
```
Remove-AzActionGroup -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="238d2-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="238d2-106">ByResourceId</span></span>
```
Remove-AzActionGroup -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="238d2-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="238d2-107">ByInputObject</span></span>
```
Remove-AzActionGroup -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="238d2-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="238d2-108">DESCRIPTION</span></span>
<span data-ttu-id="238d2-109">Das **Cmdlet "Remove-AzActionGroup"** entfernt eine Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="238d2-109">The **Remove-AzActionGroup** cmdlet removes an action group.</span></span>

## <span data-ttu-id="238d2-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="238d2-110">EXAMPLES</span></span>

### <span data-ttu-id="238d2-111">Beispiel 1: Entfernen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="238d2-111">Example 1: Remove an action group</span></span>
```
PS C:\>Remove-AzActionGroup -ResourceGroup "Default-Web-CentralUS" -Name "myActionGroup"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

## <span data-ttu-id="238d2-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="238d2-112">PARAMETERS</span></span>

### <span data-ttu-id="238d2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="238d2-113">-DefaultProfile</span></span>
<span data-ttu-id="238d2-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="238d2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="238d2-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="238d2-115">-InputObject</span></span>
<span data-ttu-id="238d2-116">Die Aktionsgrupperessource</span><span class="sxs-lookup"><span data-stu-id="238d2-116">The action group resource</span></span>

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

### <span data-ttu-id="238d2-117">-Name</span><span class="sxs-lookup"><span data-stu-id="238d2-117">-Name</span></span>
<span data-ttu-id="238d2-118">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="238d2-118">The name of the action group.</span></span>

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

### <span data-ttu-id="238d2-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="238d2-119">-ResourceGroupName</span></span>
<span data-ttu-id="238d2-120">Die Ressourcengruppe nam</span><span class="sxs-lookup"><span data-stu-id="238d2-120">The resource group nam</span></span>

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

### <span data-ttu-id="238d2-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="238d2-121">-ResourceId</span></span>
<span data-ttu-id="238d2-122">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="238d2-122">The resource i</span></span>

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

### <span data-ttu-id="238d2-123">-Confirm</span><span class="sxs-lookup"><span data-stu-id="238d2-123">-Confirm</span></span>
<span data-ttu-id="238d2-124">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="238d2-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="238d2-125">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="238d2-125">-WhatIf</span></span>
<span data-ttu-id="238d2-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="238d2-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="238d2-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="238d2-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="238d2-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="238d2-128">CommonParameters</span></span>
<span data-ttu-id="238d2-129">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="238d2-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="238d2-130">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="238d2-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="238d2-131">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="238d2-131">INPUTS</span></span>

### <span data-ttu-id="238d2-132">System.String</span><span class="sxs-lookup"><span data-stu-id="238d2-132">System.String</span></span>

### <span data-ttu-id="238d2-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="238d2-133">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="238d2-134">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="238d2-134">OUTPUTS</span></span>

### <span data-ttu-id="238d2-135">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="238d2-135">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="238d2-136">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="238d2-136">NOTES</span></span>

## <span data-ttu-id="238d2-137">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="238d2-137">RELATED LINKS</span></span>

<span data-ttu-id="238d2-138">[Set-AzActionGroup](./Set-AzActionGroup.md) 
 [Get-AzActionGroup](./Get-AzActionGroup.md) 
 [New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="238d2-138">[Set-AzActionGroup](./Set-AzActionGroup.md)
[Get-AzActionGroup](./Get-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
