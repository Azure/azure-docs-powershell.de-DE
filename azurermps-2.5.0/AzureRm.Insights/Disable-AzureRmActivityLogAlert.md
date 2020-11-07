---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
ms.openlocfilehash: dd84c2b12af850cc38770243df74a6bd25c205f3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848848"
---
# <span data-ttu-id="feabb-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="feabb-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="feabb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="feabb-102">SYNOPSIS</span></span>
<span data-ttu-id="feabb-103">Deaktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="feabb-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="feabb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="feabb-104">SYNTAX</span></span>

### <span data-ttu-id="feabb-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feabb-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="feabb-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="feabb-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="feabb-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="feabb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="feabb-108">DESCRIPTION</span></span>
<span data-ttu-id="feabb-109">Das Cmdlet **Disable-AzureRmActivityLogAlert deaktiviert** und Aktivitätsprotokoll Warnung und ermöglicht das Festlegen von Tags.</span><span class="sxs-lookup"><span data-stu-id="feabb-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="feabb-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="feabb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="feabb-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="feabb-111">EXAMPLES</span></span>

### <span data-ttu-id="feabb-112">Beispiel 1: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="feabb-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="feabb-113">Mit diesem Befehl wird die Aktivitätsprotokoll Benachrichtigung namens alert1 in der Ressourcengruppe default-ActivityLogsAlerts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="feabb-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="feabb-114">Mit diesem Befehl wird die Tags-Eigenschaft der Aktivitätsprotokoll Benachrichtigung namens alert1 geändert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="feabb-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="feabb-115">Beispiel 2: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="feabb-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="feabb-116">Mit diesem Befehl wird eine Aktivitätsprotokoll Benachrichtigung mit dem Namen alert1 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="feabb-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="feabb-117">Dafür wird ein PSActivityLogAlertResource-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="feabb-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="feabb-118">Beispiel 3: Deaktivieren der ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="feabb-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="feabb-119">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="feabb-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="feabb-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="feabb-120">PARAMETERS</span></span>

### <span data-ttu-id="feabb-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="feabb-121">-DefaultProfile</span></span>
<span data-ttu-id="feabb-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="feabb-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="feabb-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="feabb-123">-InputObject</span></span>
<span data-ttu-id="feabb-124">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tag-Eigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="feabb-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="feabb-125">-Name</span><span class="sxs-lookup"><span data-stu-id="feabb-125">-Name</span></span>
<span data-ttu-id="feabb-126">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="feabb-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="feabb-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="feabb-127">-ResourceGroupName</span></span>
<span data-ttu-id="feabb-128">Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.</span><span class="sxs-lookup"><span data-stu-id="feabb-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="feabb-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="feabb-129">-ResourceId</span></span>
<span data-ttu-id="feabb-130">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="feabb-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="feabb-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="feabb-131">-Confirm</span></span>
<span data-ttu-id="feabb-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="feabb-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="feabb-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="feabb-133">-WhatIf</span></span>
<span data-ttu-id="feabb-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="feabb-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="feabb-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="feabb-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="feabb-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="feabb-136">CommonParameters</span></span>
<span data-ttu-id="feabb-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="feabb-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="feabb-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="feabb-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="feabb-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="feabb-139">INPUTS</span></span>

### <span data-ttu-id="feabb-140">System. String</span><span class="sxs-lookup"><span data-stu-id="feabb-140">System.String</span></span>

### <span data-ttu-id="feabb-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="feabb-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="feabb-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="feabb-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="feabb-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="feabb-143">OUTPUTS</span></span>

### <span data-ttu-id="feabb-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="feabb-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="feabb-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="feabb-145">NOTES</span></span>

## <span data-ttu-id="feabb-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="feabb-146">RELATED LINKS</span></span>

[<span data-ttu-id="feabb-147">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="feabb-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="feabb-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="feabb-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="feabb-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="feabb-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="feabb-150">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="feabb-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="feabb-151">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="feabb-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="feabb-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="feabb-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
