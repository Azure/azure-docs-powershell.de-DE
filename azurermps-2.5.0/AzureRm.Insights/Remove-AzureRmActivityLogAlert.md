---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: 1dfd435d2797ee7430349546a5d2ba6fa2fe0023
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93849320"
---
# <span data-ttu-id="2eb33-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2eb33-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="2eb33-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="2eb33-102">SYNOPSIS</span></span>
<span data-ttu-id="2eb33-103">Entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2eb33-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2eb33-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="2eb33-104">SYNTAX</span></span>

### <span data-ttu-id="2eb33-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2eb33-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb33-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="2eb33-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2eb33-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="2eb33-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2eb33-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2eb33-108">DESCRIPTION</span></span>
<span data-ttu-id="2eb33-109">Das Cmdlet **Remove-AzureRmActivityLogAlert** entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2eb33-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="2eb33-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="2eb33-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="2eb33-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="2eb33-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="2eb33-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="2eb33-112">EXAMPLES</span></span>

### <span data-ttu-id="2eb33-113">Beispiel 1: Entfernen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="2eb33-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="2eb33-114">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit Name und Ressourcengruppenname als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="2eb33-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="2eb33-115">Beispiel 2: Entfernen einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe</span><span class="sxs-lookup"><span data-stu-id="2eb33-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="2eb33-116">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="2eb33-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="2eb33-117">Beispiel 3: Entfernen des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="2eb33-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="2eb33-118">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe entfernt.</span><span class="sxs-lookup"><span data-stu-id="2eb33-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="2eb33-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="2eb33-119">PARAMETERS</span></span>

### <span data-ttu-id="2eb33-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2eb33-120">-DefaultProfile</span></span>
<span data-ttu-id="2eb33-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="2eb33-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2eb33-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="2eb33-122">-InputObject</span></span>
<span data-ttu-id="2eb33-123">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um die Eigenschaften erforderlicher Name und Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2eb33-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

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

### <span data-ttu-id="2eb33-124">-Name</span><span class="sxs-lookup"><span data-stu-id="2eb33-124">-Name</span></span>
<span data-ttu-id="2eb33-125">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="2eb33-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="2eb33-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2eb33-126">-ResourceGroupName</span></span>
<span data-ttu-id="2eb33-127">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="2eb33-127">The name of the resource group where the alert resource exists.</span></span>

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

### <span data-ttu-id="2eb33-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="2eb33-128">-ResourceId</span></span>
<span data-ttu-id="2eb33-129">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="2eb33-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="2eb33-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="2eb33-130">-Confirm</span></span>
<span data-ttu-id="2eb33-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="2eb33-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2eb33-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2eb33-132">-WhatIf</span></span>
<span data-ttu-id="2eb33-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="2eb33-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2eb33-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="2eb33-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2eb33-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2eb33-135">CommonParameters</span></span>
<span data-ttu-id="2eb33-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2eb33-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2eb33-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2eb33-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2eb33-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="2eb33-138">INPUTS</span></span>

### <span data-ttu-id="2eb33-139">System. String</span><span class="sxs-lookup"><span data-stu-id="2eb33-139">System.String</span></span>

### <span data-ttu-id="2eb33-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2eb33-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="2eb33-141">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2eb33-141">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2eb33-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="2eb33-142">OUTPUTS</span></span>

### <span data-ttu-id="2eb33-143">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2eb33-143">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2eb33-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="2eb33-144">NOTES</span></span>

## <span data-ttu-id="2eb33-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="2eb33-145">RELATED LINKS</span></span>

[<span data-ttu-id="2eb33-146">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2eb33-146">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2eb33-147">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2eb33-147">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2eb33-148">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2eb33-148">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2eb33-149">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2eb33-149">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2eb33-150">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2eb33-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="2eb33-151">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2eb33-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

