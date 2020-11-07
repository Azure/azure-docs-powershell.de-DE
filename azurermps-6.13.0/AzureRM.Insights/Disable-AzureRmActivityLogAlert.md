---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/disable-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 42107266ba38dff03c77336f14015853ef9b56c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662931"
---
# <span data-ttu-id="36f1c-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="36f1c-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="36f1c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36f1c-102">SYNOPSIS</span></span>
<span data-ttu-id="36f1c-103">Deaktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="36f1c-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="36f1c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36f1c-104">SYNTAX</span></span>

### <span data-ttu-id="36f1c-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="36f1c-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f1c-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="36f1c-106">DisableByInputObject</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="36f1c-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="36f1c-107">DisableByResourceId</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="36f1c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36f1c-108">DESCRIPTION</span></span>
<span data-ttu-id="36f1c-109">Das Cmdlet **Disable-AzureRmActivityLogAlert deaktiviert** und Aktivitätsprotokoll Warnung und ermöglicht das Festlegen von Tags.</span><span class="sxs-lookup"><span data-stu-id="36f1c-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="36f1c-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="36f1c-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="36f1c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36f1c-111">EXAMPLES</span></span>

### <span data-ttu-id="36f1c-112">Beispiel 1: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="36f1c-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="36f1c-113">Mit diesem Befehl wird die Aktivitätsprotokoll Benachrichtigung namens alert1 in der Ressourcengruppe default-ActivityLogsAlerts deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="36f1c-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="36f1c-114">Mit diesem Befehl wird die Tags-Eigenschaft der Aktivitätsprotokoll Benachrichtigung namens alert1 geändert und deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="36f1c-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="36f1c-115">Beispiel 2: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="36f1c-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="36f1c-116">Mit diesem Befehl wird eine Aktivitätsprotokoll Benachrichtigung mit dem Namen alert1 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="36f1c-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="36f1c-117">Dafür wird ein PSActivityLogAlertResource-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="36f1c-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="36f1c-118">Beispiel 3: Deaktivieren der ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="36f1c-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="36f1c-119">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="36f1c-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="36f1c-120">Parameter</span><span class="sxs-lookup"><span data-stu-id="36f1c-120">PARAMETERS</span></span>

### <span data-ttu-id="36f1c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36f1c-121">-DefaultProfile</span></span>
<span data-ttu-id="36f1c-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="36f1c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="36f1c-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="36f1c-123">-InputObject</span></span>
<span data-ttu-id="36f1c-124">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tag-Eigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="36f1c-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

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

### <span data-ttu-id="36f1c-125">-Name</span><span class="sxs-lookup"><span data-stu-id="36f1c-125">-Name</span></span>
<span data-ttu-id="36f1c-126">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="36f1c-126">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="36f1c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36f1c-127">-ResourceGroupName</span></span>
<span data-ttu-id="36f1c-128">Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.</span><span class="sxs-lookup"><span data-stu-id="36f1c-128">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="36f1c-129">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="36f1c-129">-ResourceId</span></span>
<span data-ttu-id="36f1c-130">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="36f1c-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="36f1c-131">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="36f1c-131">-Confirm</span></span>
<span data-ttu-id="36f1c-132">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="36f1c-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="36f1c-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="36f1c-133">-WhatIf</span></span>
<span data-ttu-id="36f1c-134">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="36f1c-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="36f1c-135">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="36f1c-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="36f1c-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36f1c-136">CommonParameters</span></span>
<span data-ttu-id="36f1c-137">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36f1c-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36f1c-138">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36f1c-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36f1c-139">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36f1c-139">INPUTS</span></span>

### <span data-ttu-id="36f1c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="36f1c-140">System.String</span></span>

### <span data-ttu-id="36f1c-141">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="36f1c-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>
<span data-ttu-id="36f1c-142">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="36f1c-142">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="36f1c-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36f1c-143">OUTPUTS</span></span>

### <span data-ttu-id="36f1c-144">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="36f1c-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="36f1c-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="36f1c-145">NOTES</span></span>

## <span data-ttu-id="36f1c-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36f1c-146">RELATED LINKS</span></span>

[<span data-ttu-id="36f1c-147">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="36f1c-147">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="36f1c-148">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="36f1c-148">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="36f1c-149">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="36f1c-149">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="36f1c-150">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="36f1c-150">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="36f1c-151">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="36f1c-151">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="36f1c-152">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="36f1c-152">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
