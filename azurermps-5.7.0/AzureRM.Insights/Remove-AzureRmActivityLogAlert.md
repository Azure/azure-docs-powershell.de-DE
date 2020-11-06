---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/remove-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: b712363b2b4e1d610f00f1111c48145debe084a6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500586"
---
# <span data-ttu-id="9ec48-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9ec48-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9ec48-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="9ec48-102">SYNOPSIS</span></span>
<span data-ttu-id="9ec48-103">Entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9ec48-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9ec48-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="9ec48-104">SYNTAX</span></span>

### <span data-ttu-id="9ec48-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="9ec48-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec48-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="9ec48-106">RemoveByInputObject</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9ec48-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="9ec48-107">RemoveByResourceId</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ec48-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9ec48-108">DESCRIPTION</span></span>
<span data-ttu-id="9ec48-109">Das Cmdlet **Remove-AzureRmActivityLogAlert** entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9ec48-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="9ec48-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="9ec48-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

<span data-ttu-id="9ec48-111">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich erstellt, geändert oder entfernt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec48-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="9ec48-112">Beispiele</span><span class="sxs-lookup"><span data-stu-id="9ec48-112">EXAMPLES</span></span>

### <span data-ttu-id="9ec48-113">Beispiel 1: Entfernen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="9ec48-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="9ec48-114">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit Name und Ressourcengruppenname als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9ec48-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="9ec48-115">Beispiel 2: Entfernen einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe</span><span class="sxs-lookup"><span data-stu-id="9ec48-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="9ec48-116">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="9ec48-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="9ec48-117">Beispiel 3: Entfernen des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec48-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="9ec48-118">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe entfernt.</span><span class="sxs-lookup"><span data-stu-id="9ec48-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="9ec48-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="9ec48-119">PARAMETERS</span></span>

### <span data-ttu-id="9ec48-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ec48-120">-DefaultProfile</span></span>
<span data-ttu-id="9ec48-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="9ec48-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-122">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="9ec48-122">-InputObject</span></span>
<span data-ttu-id="9ec48-123">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um die Eigenschaften erforderlicher Name und Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="9ec48-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-124">-Name</span><span class="sxs-lookup"><span data-stu-id="9ec48-124">-Name</span></span>
<span data-ttu-id="9ec48-125">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="9ec48-125">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ec48-126">-ResourceGroupName</span></span>
<span data-ttu-id="9ec48-127">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9ec48-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-128">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="9ec48-128">-ResourceId</span></span>
<span data-ttu-id="9ec48-129">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="9ec48-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByResourceId
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="9ec48-130">-Confirm</span></span>
<span data-ttu-id="9ec48-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9ec48-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ec48-132">-WhatIf</span></span>
<span data-ttu-id="9ec48-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9ec48-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ec48-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9ec48-134">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9ec48-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ec48-135">CommonParameters</span></span>
<span data-ttu-id="9ec48-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9ec48-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ec48-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9ec48-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ec48-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="9ec48-138">INPUTS</span></span>

### <span data-ttu-id="9ec48-139">Keine</span><span class="sxs-lookup"><span data-stu-id="9ec48-139">None</span></span>
<span data-ttu-id="9ec48-140">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="9ec48-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9ec48-141">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="9ec48-141">OUTPUTS</span></span>

### <span data-ttu-id="9ec48-142">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="9ec48-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="9ec48-143">Notizen</span><span class="sxs-lookup"><span data-stu-id="9ec48-143">NOTES</span></span>

## <span data-ttu-id="9ec48-144">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="9ec48-144">RELATED LINKS</span></span>

[<span data-ttu-id="9ec48-145">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9ec48-145">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9ec48-146">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9ec48-146">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9ec48-147">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9ec48-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9ec48-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9ec48-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9ec48-149">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9ec48-149">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9ec48-150">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9ec48-150">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

