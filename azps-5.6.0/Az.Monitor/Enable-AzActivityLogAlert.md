---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: ece935169efab8a550312a97d3ebad21a133b04f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101932728"
---
# <span data-ttu-id="94453-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="94453-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="94453-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="94453-102">SYNOPSIS</span></span>
<span data-ttu-id="94453-103">Aktiviert eine Aktivitätsprotokollbenachrichtigung und legt deren Tags fest.</span><span class="sxs-lookup"><span data-stu-id="94453-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="94453-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="94453-104">SYNTAX</span></span>

### <span data-ttu-id="94453-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="94453-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94453-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="94453-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="94453-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="94453-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="94453-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="94453-108">DESCRIPTION</span></span>
<span data-ttu-id="94453-109">Das **Enable-AzActivityLogAlert-Cmdlet** ermöglicht das Aktivieren einer Aktivitätsprotokollbenachrichtigung und das Festlegen der Tags.</span><span class="sxs-lookup"><span data-stu-id="94453-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="94453-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h. es kann eine Bestätigung vom Benutzer anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="94453-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="94453-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="94453-111">EXAMPLES</span></span>

### <span data-ttu-id="94453-112">Beispiel 1: Aktivieren einer Aktivitätsprotokollbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="94453-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="94453-113">Dieser Befehl aktiviert die Aktivitätsprotokollbenachrichtigung mit dem Namen warnung1 in der Ressourcengruppe Default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="94453-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="94453-114">Beispiel 2: Aktivieren einer Aktivitätsprotokollbenachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="94453-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="94453-115">Mit diesem Befehl wird eine Aktivitätsprotokollbenachrichtigung mit dem Namen "Warnung1" aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94453-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="94453-116">Dazu verwendet es ein PSActivityLogAlertResource-Objekt als Eingabeargument.</span><span class="sxs-lookup"><span data-stu-id="94453-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="94453-117">Beispiel 3: Aktivieren des ActivityLogAlert mithilfe des Parameters ResourceId</span><span class="sxs-lookup"><span data-stu-id="94453-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="94453-118">Mit diesem Befehl wird der ActivityLogAlert mithilfe des Parameters ResourceId aus der Pipe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="94453-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="94453-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="94453-119">PARAMETERS</span></span>

### <span data-ttu-id="94453-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="94453-120">-DefaultProfile</span></span>
<span data-ttu-id="94453-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="94453-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="94453-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="94453-122">-InputObject</span></span>
<span data-ttu-id="94453-123">Legt die InputObject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tagseigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="94453-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="94453-124">-Name</span><span class="sxs-lookup"><span data-stu-id="94453-124">-Name</span></span>
<span data-ttu-id="94453-125">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="94453-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="94453-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="94453-126">-ResourceGroupName</span></span>
<span data-ttu-id="94453-127">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="94453-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="94453-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="94453-128">-ResourceId</span></span>
<span data-ttu-id="94453-129">Legt die ResourceId-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, die Eigenschaften des Ressourcengruppennamens zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="94453-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="94453-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="94453-130">-Confirm</span></span>
<span data-ttu-id="94453-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="94453-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="94453-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="94453-132">-WhatIf</span></span>
<span data-ttu-id="94453-133">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="94453-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="94453-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="94453-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="94453-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="94453-135">CommonParameters</span></span>
<span data-ttu-id="94453-136">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="94453-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="94453-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="94453-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="94453-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="94453-138">INPUTS</span></span>

### <span data-ttu-id="94453-139">System.String</span><span class="sxs-lookup"><span data-stu-id="94453-139">System.String</span></span>

### <span data-ttu-id="94453-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="94453-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="94453-141">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="94453-141">OUTPUTS</span></span>

### <span data-ttu-id="94453-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="94453-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="94453-143">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="94453-143">NOTES</span></span>

## <span data-ttu-id="94453-144">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="94453-144">RELATED LINKS</span></span>

[<span data-ttu-id="94453-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="94453-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="94453-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="94453-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="94453-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="94453-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="94453-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="94453-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="94453-149">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="94453-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="94453-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="94453-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
