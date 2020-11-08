---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: 5a0841a3cb2cd01ebb7f44b41e89d0b30404dfd0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/21/2020
ms.locfileid: "93995083"
---
# <span data-ttu-id="1a186-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1a186-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="1a186-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="1a186-102">SYNOPSIS</span></span>
<span data-ttu-id="1a186-103">Entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1a186-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="1a186-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="1a186-104">SYNTAX</span></span>

### <span data-ttu-id="1a186-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="1a186-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a186-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="1a186-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1a186-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="1a186-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1a186-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1a186-108">DESCRIPTION</span></span>
<span data-ttu-id="1a186-109">Das Cmdlet **Remove-AzActivityLogAlert** entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1a186-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="1a186-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="1a186-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="1a186-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="1a186-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="1a186-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="1a186-112">EXAMPLES</span></span>

### <span data-ttu-id="1a186-113">Beispiel 1: Entfernen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="1a186-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="1a186-114">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit Name und Ressourcengruppenname als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="1a186-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="1a186-115">Beispiel 2: Entfernen einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe</span><span class="sxs-lookup"><span data-stu-id="1a186-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="1a186-116">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="1a186-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="1a186-117">Beispiel 3: Entfernen des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="1a186-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="1a186-118">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe entfernt.</span><span class="sxs-lookup"><span data-stu-id="1a186-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="1a186-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a186-119">PARAMETERS</span></span>

### <span data-ttu-id="1a186-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a186-120">-DefaultProfile</span></span>
<span data-ttu-id="1a186-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="1a186-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a186-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="1a186-122">-InputObject</span></span>
<span data-ttu-id="1a186-123">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um die Eigenschaften erforderlicher Name und Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="1a186-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="1a186-124">-Name</span><span class="sxs-lookup"><span data-stu-id="1a186-124">-Name</span></span>
<span data-ttu-id="1a186-125">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="1a186-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="1a186-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a186-126">-ResourceGroupName</span></span>
<span data-ttu-id="1a186-127">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="1a186-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="1a186-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="1a186-128">-ResourceId</span></span>
<span data-ttu-id="1a186-129">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="1a186-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="1a186-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="1a186-130">-Confirm</span></span>
<span data-ttu-id="1a186-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="1a186-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1a186-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1a186-132">-WhatIf</span></span>
<span data-ttu-id="1a186-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="1a186-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1a186-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="1a186-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1a186-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a186-135">CommonParameters</span></span>
<span data-ttu-id="1a186-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1a186-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a186-137">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1a186-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a186-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="1a186-138">INPUTS</span></span>

### <span data-ttu-id="1a186-139">System. String</span><span class="sxs-lookup"><span data-stu-id="1a186-139">System.String</span></span>

### <span data-ttu-id="1a186-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1a186-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1a186-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="1a186-141">OUTPUTS</span></span>

### <span data-ttu-id="1a186-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="1a186-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="1a186-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="1a186-143">NOTES</span></span>

## <span data-ttu-id="1a186-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="1a186-144">RELATED LINKS</span></span>

[<span data-ttu-id="1a186-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1a186-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="1a186-146">Deaktivieren-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1a186-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="1a186-147">Satz-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1a186-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="1a186-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1a186-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="1a186-149">Neu – AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="1a186-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="1a186-150">Neu – AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1a186-150">New-AzActivityLogAlertCondition</span></span>](./Get-AzActivityLogAlertCondition.md)

