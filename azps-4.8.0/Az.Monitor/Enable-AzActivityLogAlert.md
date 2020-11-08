---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94173699"
---
# <span data-ttu-id="f7578-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f7578-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="f7578-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f7578-102">SYNOPSIS</span></span>
<span data-ttu-id="f7578-103">Aktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="f7578-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="f7578-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f7578-104">SYNTAX</span></span>

### <span data-ttu-id="f7578-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="f7578-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7578-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="f7578-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7578-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="f7578-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7578-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7578-108">DESCRIPTION</span></span>
<span data-ttu-id="f7578-109">Das Cmdlet **enable-AzActivityLogAlert** ermöglicht es, eine Aktivitätsprotokoll Benachrichtigung zu aktivieren und Ihre Tags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="f7578-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="f7578-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="f7578-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="f7578-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f7578-111">EXAMPLES</span></span>

### <span data-ttu-id="f7578-112">Beispiel 1: Aktivieren einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="f7578-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="f7578-113">Dieser Befehl aktiviert die Aktivitätsprotokoll Benachrichtigung namens alert1 in der Ressourcengruppe default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="f7578-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="f7578-114">Beispiel 2: Aktivieren einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="f7578-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="f7578-115">Mit diesem Befehl wird eine Aktivitätsprotokoll Benachrichtigung mit dem Namen alert1 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7578-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="f7578-116">Dafür wird ein PSActivityLogAlertResource-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="f7578-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="f7578-117">Beispiel 3: Aktivieren des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="f7578-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="f7578-118">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f7578-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="f7578-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="f7578-119">PARAMETERS</span></span>

### <span data-ttu-id="f7578-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7578-120">-DefaultProfile</span></span>
<span data-ttu-id="f7578-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="f7578-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f7578-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f7578-122">-InputObject</span></span>
<span data-ttu-id="f7578-123">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tags-Eigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="f7578-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="f7578-124">-Name</span><span class="sxs-lookup"><span data-stu-id="f7578-124">-Name</span></span>
<span data-ttu-id="f7578-125">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="f7578-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="f7578-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f7578-126">-ResourceGroupName</span></span>
<span data-ttu-id="f7578-127">Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.</span><span class="sxs-lookup"><span data-stu-id="f7578-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="f7578-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="f7578-128">-ResourceId</span></span>
<span data-ttu-id="f7578-129">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="f7578-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="f7578-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="f7578-130">-Confirm</span></span>
<span data-ttu-id="f7578-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f7578-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7578-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7578-132">-WhatIf</span></span>
<span data-ttu-id="f7578-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="f7578-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f7578-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f7578-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7578-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7578-135">CommonParameters</span></span>
<span data-ttu-id="f7578-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f7578-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7578-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f7578-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7578-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f7578-138">INPUTS</span></span>

### <span data-ttu-id="f7578-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f7578-139">System.String</span></span>

### <span data-ttu-id="f7578-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f7578-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f7578-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f7578-141">OUTPUTS</span></span>

### <span data-ttu-id="f7578-142">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="f7578-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="f7578-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="f7578-143">NOTES</span></span>

## <span data-ttu-id="f7578-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f7578-144">RELATED LINKS</span></span>

[<span data-ttu-id="f7578-145">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f7578-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="f7578-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f7578-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="f7578-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f7578-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="f7578-148">Neu – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="f7578-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="f7578-149">Neu – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f7578-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="f7578-150">Deaktivieren-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f7578-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
