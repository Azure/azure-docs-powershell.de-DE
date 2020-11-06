---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Enable-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92607537fb80132627e1f26f240a10b8f7150fb8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93504945"
---
# <span data-ttu-id="b3dba-101">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3dba-101">Enable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="b3dba-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="b3dba-102">SYNOPSIS</span></span>
<span data-ttu-id="b3dba-103">Aktiviert eine Aktivitätsprotokoll Benachrichtigung und legt ihre Tags fest.</span><span class="sxs-lookup"><span data-stu-id="b3dba-103">Enables an activity log alert and sets its Tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b3dba-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="b3dba-104">SYNTAX</span></span>

### <span data-ttu-id="b3dba-105">Standardparameter für das Aktivieren einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b3dba-105">Default parameters for enable an activity log alert</span></span>
```
Enable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3dba-106">Parameter zum Aktivieren einer Aktivitätsprotokoll Benachrichtigung, die den Wert aus der Pipe nimmt</span><span class="sxs-lookup"><span data-stu-id="b3dba-106">Parameters to enable an activity log alerts taking value from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b3dba-107">Parameter zum Aktivieren einer Aktivitätsprotokoll Benachrichtigung, wobei der Wert der Resourcen-Funktion aus der Pipe genommen wird</span><span class="sxs-lookup"><span data-stu-id="b3dba-107">Parameters to enable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Enable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b3dba-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3dba-108">DESCRIPTION</span></span>
<span data-ttu-id="b3dba-109">Das Cmdlet **enable-AzureRmActivityLogAlert** ermöglicht es, eine Aktivitätsprotokoll Benachrichtigung zu aktivieren und Ihre Tags festzulegen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-109">The **Enable-AzureRmActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="b3dba-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="b3dba-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="b3dba-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="b3dba-111">EXAMPLES</span></span>

### <span data-ttu-id="b3dba-112">Beispiel 1: Deaktivieren einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="b3dba-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Enable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="b3dba-113">Dieser Befehl aktiviert die Aktivitätsprotokoll Benachrichtigung namens alert1 in der Ressourcengruppe default-ActivityLogsAlerts.</span><span class="sxs-lookup"><span data-stu-id="b3dba-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="b3dba-114">Beispiel 2: Aktivieren einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource-Objekt als Eingabe</span><span class="sxs-lookup"><span data-stu-id="b3dba-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="b3dba-115">Mit diesem Befehl wird eine Aktivitätsprotokoll Benachrichtigung mit dem Namen alert1 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3dba-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="b3dba-116">Dafür wird ein PSActivityLogAlertResource-Objekt als Eingabeargument verwendet.</span><span class="sxs-lookup"><span data-stu-id="b3dba-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="b3dba-117">Beispiel 3: Aktivieren des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="b3dba-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Enable-AzureRmActivityLogAlert
```

<span data-ttu-id="b3dba-118">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b3dba-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="b3dba-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3dba-119">PARAMETERS</span></span>

### <span data-ttu-id="b3dba-120">-Name</span><span class="sxs-lookup"><span data-stu-id="b3dba-120">-Name</span></span>
<span data-ttu-id="b3dba-121">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="b3dba-121">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dba-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3dba-122">-ResourceGroupName</span></span>
<span data-ttu-id="b3dba-123">Der Name der Ressourcengruppe, in der die Benachrichtigungs Ressource vorhanden sein wird.</span><span class="sxs-lookup"><span data-stu-id="b3dba-123">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for enable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dba-124">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="b3dba-124">-InputObject</span></span>
<span data-ttu-id="b3dba-125">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um den erforderlichen Namen, den Ressourcengruppennamen und die optionalen Tags-Eigenschaften zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="b3dba-125">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to enable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dba-126">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="b3dba-126">-ResourceId</span></span>
<span data-ttu-id="b3dba-127">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="b3dba-127">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to enable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3dba-128">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="b3dba-128">-Confirm</span></span>
<span data-ttu-id="b3dba-129">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="b3dba-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3dba-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3dba-130">-DefaultProfile</span></span>
<span data-ttu-id="b3dba-131">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="b3dba-131">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3dba-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3dba-132">-WhatIf</span></span>
<span data-ttu-id="b3dba-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="b3dba-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b3dba-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="b3dba-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3dba-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3dba-135">CommonParameters</span></span>
<span data-ttu-id="b3dba-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3dba-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3dba-137">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b3dba-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3dba-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="b3dba-138">INPUTS</span></span>

## <span data-ttu-id="b3dba-139">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="b3dba-139">OUTPUTS</span></span>

### <span data-ttu-id="b3dba-140">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="b3dba-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="b3dba-141">Notizen</span><span class="sxs-lookup"><span data-stu-id="b3dba-141">NOTES</span></span>

## <span data-ttu-id="b3dba-142">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="b3dba-142">RELATED LINKS</span></span>

[<span data-ttu-id="b3dba-143">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3dba-143">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b3dba-144">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3dba-144">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b3dba-145">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3dba-145">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="b3dba-146">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="b3dba-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="b3dba-147">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="b3dba-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="b3dba-148">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="b3dba-148">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)
