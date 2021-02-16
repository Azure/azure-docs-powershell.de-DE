---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 999a56358f764909dcf6cbad2d3816c979d34bbb
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399293"
---
# <span data-ttu-id="917f7-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="917f7-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="917f7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="917f7-102">SYNOPSIS</span></span>
<span data-ttu-id="917f7-103">Entfernt eine Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="917f7-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="917f7-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="917f7-104">SYNTAX</span></span>

### <span data-ttu-id="917f7-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="917f7-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="917f7-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="917f7-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="917f7-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="917f7-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="917f7-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="917f7-108">DESCRIPTION</span></span>
<span data-ttu-id="917f7-109">Das **Cmdlet "Remove-AzActivityLogAlert"** entfernt eine Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="917f7-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="917f7-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor tatsächlich ein Patchen der Ressource implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="917f7-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="917f7-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="917f7-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="917f7-112">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="917f7-112">EXAMPLES</span></span>

### <span data-ttu-id="917f7-113">Beispiel 1: Entfernen einer Aktivitätsprotokollbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="917f7-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="917f7-114">Entfernt eine Aktivitätsprotokollbenachrichtigung unter Verwendung des Namens und des Ressourcengruppennamens als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="917f7-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="917f7-115">Beispiel 2: Entfernen einer Aktivitätsprotokollbenachrichtigung mit einer PSActivityLogAlertResource als Eingabe</span><span class="sxs-lookup"><span data-stu-id="917f7-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="917f7-116">Entfernt eine Aktivitätsprotokollbenachrichtigung, indem eine PSActivityLogAlertResource als Eingabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="917f7-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="917f7-117">Beispiel 3: Entfernen von "ActivityLogAlert" mit dem Parameter "ResourceId"</span><span class="sxs-lookup"><span data-stu-id="917f7-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="917f7-118">Mit diesem Befehl wird "ActivityLogAlert" mithilfe des Parameters "ResourceId" aus dem Pipe entfernt.</span><span class="sxs-lookup"><span data-stu-id="917f7-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="917f7-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="917f7-119">PARAMETERS</span></span>

### <span data-ttu-id="917f7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="917f7-120">-DefaultProfile</span></span>
<span data-ttu-id="917f7-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="917f7-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="917f7-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="917f7-122">-InputObject</span></span>
<span data-ttu-id="917f7-123">Legt die Eigenschaft der InputObject-Tags des Aufrufs fest, um den erforderlichen Namen und die Eigenschaften des Ressourcengruppennamens zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="917f7-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="917f7-124">-Name</span><span class="sxs-lookup"><span data-stu-id="917f7-124">-Name</span></span>
<span data-ttu-id="917f7-125">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="917f7-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="917f7-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="917f7-126">-ResourceGroupName</span></span>
<span data-ttu-id="917f7-127">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="917f7-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="917f7-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="917f7-128">-ResourceId</span></span>
<span data-ttu-id="917f7-129">Legt die Eigenschaft der Tags "ResourceId" des Aufrufs fest, um die Eigenschaften des erforderlichen Namens und der Ressourcengruppe zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="917f7-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="917f7-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="917f7-130">-Confirm</span></span>
<span data-ttu-id="917f7-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="917f7-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="917f7-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="917f7-132">-WhatIf</span></span>
<span data-ttu-id="917f7-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="917f7-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="917f7-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="917f7-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="917f7-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="917f7-135">CommonParameters</span></span>
<span data-ttu-id="917f7-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="917f7-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="917f7-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="917f7-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="917f7-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="917f7-138">INPUTS</span></span>

### <span data-ttu-id="917f7-139">System.String</span><span class="sxs-lookup"><span data-stu-id="917f7-139">System.String</span></span>

### <span data-ttu-id="917f7-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="917f7-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="917f7-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="917f7-141">OUTPUTS</span></span>

### <span data-ttu-id="917f7-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="917f7-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="917f7-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="917f7-143">NOTES</span></span>

## <span data-ttu-id="917f7-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="917f7-144">RELATED LINKS</span></span>

[<span data-ttu-id="917f7-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="917f7-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="917f7-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="917f7-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="917f7-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="917f7-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="917f7-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="917f7-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="917f7-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="917f7-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



