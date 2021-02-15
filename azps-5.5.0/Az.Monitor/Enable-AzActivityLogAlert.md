---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100159460"
---
# <span data-ttu-id="5700f-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5700f-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="5700f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5700f-102">SYNOPSIS</span></span>
<span data-ttu-id="5700f-103">Aktiviert eine Aktivitätsprotokollbenachrichtigung und legt deren Tags fest.</span><span class="sxs-lookup"><span data-stu-id="5700f-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="5700f-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="5700f-104">SYNTAX</span></span>

### <span data-ttu-id="5700f-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="5700f-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5700f-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="5700f-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5700f-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="5700f-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5700f-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="5700f-108">DESCRIPTION</span></span>
<span data-ttu-id="5700f-109">Das **Cmdlet "Enable-AzActivityLogAlert"** ermöglicht das Aktivieren einer Aktivitätsprotokollbenachrichtigung und das Festlegen der Tags.</span><span class="sxs-lookup"><span data-stu-id="5700f-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="5700f-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor tatsächlich ein Patchen der Ressource implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="5700f-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="5700f-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="5700f-111">EXAMPLES</span></span>

### <span data-ttu-id="5700f-112">Beispiel 1: Aktivieren einer Aktivitätsprotokollbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="5700f-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="5700f-113">Dieser Befehl aktiviert die Aktivitätsprotokollwarnung namens "warnung1" in der Ressourcengruppe "Default-ActivityLogsAlerts".</span><span class="sxs-lookup"><span data-stu-id="5700f-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="5700f-114">Beispiel 2: Aktivieren einer Aktivitätsprotokollbenachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="5700f-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="5700f-115">Dieser Befehl aktiviert eine Aktivitätsprotokollbenachrichtigung namens "Warnung1".</span><span class="sxs-lookup"><span data-stu-id="5700f-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="5700f-116">Hierin wird ein "PSActivityLogAlertResource"-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="5700f-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="5700f-117">Beispiel 3: Aktivieren von "ActivityLogAlert" mit dem Parameter "ResourceId"</span><span class="sxs-lookup"><span data-stu-id="5700f-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="5700f-118">Dieser Befehl aktiviert "ActivityLogAlert" mit dem Parameter "ResourceId" aus dem Pipe.</span><span class="sxs-lookup"><span data-stu-id="5700f-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="5700f-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5700f-119">PARAMETERS</span></span>

### <span data-ttu-id="5700f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5700f-120">-DefaultProfile</span></span>
<span data-ttu-id="5700f-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="5700f-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5700f-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5700f-122">-InputObject</span></span>
<span data-ttu-id="5700f-123">Legt die Eigenschaft der InputObject-Tags des Aufrufs fest, um den erforderlichen Namen, den Namen der Ressourcengruppe und die optionalen Tageigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="5700f-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5700f-124">-Name</span><span class="sxs-lookup"><span data-stu-id="5700f-124">-Name</span></span>
<span data-ttu-id="5700f-125">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="5700f-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5700f-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5700f-126">-ResourceGroupName</span></span>
<span data-ttu-id="5700f-127">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="5700f-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5700f-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5700f-128">-ResourceId</span></span>
<span data-ttu-id="5700f-129">Legt die Eigenschaft der Tags "ResourceId" des Aufrufs fest, um die Eigenschaften des erforderlichen Namens und der Ressourcengruppe zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="5700f-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5700f-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5700f-130">-Confirm</span></span>
<span data-ttu-id="5700f-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5700f-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5700f-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="5700f-132">-WhatIf</span></span>
<span data-ttu-id="5700f-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5700f-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5700f-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5700f-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5700f-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5700f-135">CommonParameters</span></span>
<span data-ttu-id="5700f-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5700f-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5700f-137">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5700f-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5700f-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="5700f-138">INPUTS</span></span>

### <span data-ttu-id="5700f-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5700f-139">System.String</span></span>

### <span data-ttu-id="5700f-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5700f-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5700f-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="5700f-141">OUTPUTS</span></span>

### <span data-ttu-id="5700f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="5700f-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="5700f-143">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="5700f-143">NOTES</span></span>

## <span data-ttu-id="5700f-144">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="5700f-144">RELATED LINKS</span></span>

[<span data-ttu-id="5700f-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5700f-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="5700f-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5700f-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="5700f-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5700f-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="5700f-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="5700f-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="5700f-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="5700f-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="5700f-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="5700f-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
