---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 4ce3bc8c0efd5acd4e39d61c083c82bff960066e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100409221"
---
# <span data-ttu-id="c1872-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c1872-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="c1872-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1872-102">SYNOPSIS</span></span>
<span data-ttu-id="c1872-103">Deaktiviert eine Aktivitätsprotokollbenachrichtigung und legt deren Tags fest.</span><span class="sxs-lookup"><span data-stu-id="c1872-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="c1872-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1872-104">SYNTAX</span></span>

### <span data-ttu-id="c1872-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c1872-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1872-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="c1872-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c1872-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="c1872-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c1872-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1872-108">DESCRIPTION</span></span>
<span data-ttu-id="c1872-109">Das **Cmdlet "Disable-AzActivityLogAlert"** deaktiviert und ermöglicht das Festlegen seiner Tags.</span><span class="sxs-lookup"><span data-stu-id="c1872-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="c1872-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung vom Benutzer anfordern, bevor tatsächlich ein Patchen der Ressource implementiert wird.</span><span class="sxs-lookup"><span data-stu-id="c1872-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="c1872-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1872-111">EXAMPLES</span></span>

### <span data-ttu-id="c1872-112">Beispiel 1: Deaktivieren einer Aktivitätsprotokollbenachrichtigung</span><span class="sxs-lookup"><span data-stu-id="c1872-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="c1872-113">Mit diesem Befehl wird die Aktivitätsprotokollbenachrichtigung mit dem Namen "warnung1" in der Ressourcengruppe "Default-ActivityLogsAlerts" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c1872-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="c1872-114">Mit diesem Befehl wird die Tageigenschaft der Aktivitätsprotokollbenachrichtigung namens "Warnung1" geändert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c1872-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="c1872-115">Beispiel 2: Deaktivieren einer Aktivitätsprotokollbenachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="c1872-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="c1872-116">Mit diesem Befehl wird eine Aktivitätsprotokollbenachrichtigung mit dem Namen "Warnung1" deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c1872-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="c1872-117">Hierin wird ein "PSActivityLogAlertResource"-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="c1872-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="c1872-118">Beispiel 3: Deaktivieren von "ActivityLogAlert" mit dem Parameter "ResourceId"</span><span class="sxs-lookup"><span data-stu-id="c1872-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="c1872-119">Mit diesem Befehl wird "ActivityLogAlert" mit dem Parameter "ResourceId" aus dem Pipe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c1872-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="c1872-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1872-120">PARAMETERS</span></span>

### <span data-ttu-id="c1872-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1872-121">-DefaultProfile</span></span>
<span data-ttu-id="c1872-122">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c1872-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c1872-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c1872-123">-InputObject</span></span>
<span data-ttu-id="c1872-124">Legt die Eigenschaft der InputObject-Tags des Aufrufs fest, um den erforderlichen Namen, den Namen der Ressourcengruppe und die optionalen Tageigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c1872-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c1872-125">-Name</span><span class="sxs-lookup"><span data-stu-id="c1872-125">-Name</span></span>
<span data-ttu-id="c1872-126">Der Name der Aktivitätsprotokollbenachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="c1872-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1872-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1872-127">-ResourceGroupName</span></span>
<span data-ttu-id="c1872-128">Der Name der Ressourcengruppe, in der die Warnungsressource vorhanden sein soll.</span><span class="sxs-lookup"><span data-stu-id="c1872-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1872-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c1872-129">-ResourceId</span></span>
<span data-ttu-id="c1872-130">Legt die Eigenschaft der Tags "ResourceId" des Aufrufs fest, um die Eigenschaften des erforderlichen Namens und der Ressourcengruppe zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="c1872-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c1872-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c1872-131">-Confirm</span></span>
<span data-ttu-id="c1872-132">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c1872-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c1872-133">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c1872-133">-WhatIf</span></span>
<span data-ttu-id="c1872-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c1872-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c1872-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c1872-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c1872-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1872-136">CommonParameters</span></span>
<span data-ttu-id="c1872-137">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1872-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1872-138">Weitere Informationen finden Sie unter [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c1872-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1872-139">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1872-139">INPUTS</span></span>

### <span data-ttu-id="c1872-140">System.String</span><span class="sxs-lookup"><span data-stu-id="c1872-140">System.String</span></span>

### <span data-ttu-id="c1872-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c1872-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c1872-142">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1872-142">OUTPUTS</span></span>

### <span data-ttu-id="c1872-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c1872-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c1872-144">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1872-144">NOTES</span></span>

## <span data-ttu-id="c1872-145">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1872-145">RELATED LINKS</span></span>

[<span data-ttu-id="c1872-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c1872-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="c1872-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c1872-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="c1872-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c1872-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="c1872-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="c1872-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)



[<span data-ttu-id="c1872-150">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c1872-150">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
