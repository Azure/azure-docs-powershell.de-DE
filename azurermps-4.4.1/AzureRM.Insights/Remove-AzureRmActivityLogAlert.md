---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93665380"
---
# <span data-ttu-id="29651-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="29651-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="29651-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="29651-102">SYNOPSIS</span></span>
<span data-ttu-id="29651-103">Entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="29651-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="29651-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="29651-104">SYNTAX</span></span>

### <span data-ttu-id="29651-105">Standardparameter für das Entfernen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="29651-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29651-106">Parameter zum Entfernen einer Aktivitätsprotokoll Benachrichtigung, die den Wert aus der Pipe nimmt</span><span class="sxs-lookup"><span data-stu-id="29651-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="29651-107">Parameter zum Entfernen einer Aktivitätsprotokoll Benachrichtigung, wobei der Wert der "einquellen-Nr" aus der Pipe genommen wird</span><span class="sxs-lookup"><span data-stu-id="29651-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="29651-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="29651-108">DESCRIPTION</span></span>
<span data-ttu-id="29651-109">Das Cmdlet **Remove-AzureRmActivityLogAlert** entfernt eine Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="29651-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="29651-110">Dieses Cmdlet implementiert das ShouldProcess-Muster, d. h., es kann eine Bestätigung des Benutzers anfordern, bevor die Ressource tatsächlich gepatcht wird.</span><span class="sxs-lookup"><span data-stu-id="29651-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="29651-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="29651-111">EXAMPLES</span></span>

### <span data-ttu-id="29651-112">Beispiel 1: Entfernen einer Aktivitätsprotokoll Benachrichtigung</span><span class="sxs-lookup"><span data-stu-id="29651-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="29651-113">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit Name und Ressourcengruppenname als Eingaben.</span><span class="sxs-lookup"><span data-stu-id="29651-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="29651-114">Beispiel 2: Entfernen einer Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe</span><span class="sxs-lookup"><span data-stu-id="29651-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="29651-115">Entfernt eine Aktivitätsprotokoll Benachrichtigung mit einem PSActivityLogAlertResource als Eingabe.</span><span class="sxs-lookup"><span data-stu-id="29651-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="29651-116">Beispiel 3: Entfernen des ActivityLogAlert mit dem resourcecode-Parameter</span><span class="sxs-lookup"><span data-stu-id="29651-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="29651-117">Mit diesem Befehl wird der ActivityLogAlert mit dem resourcecode-Parameter aus der Pipe entfernt.</span><span class="sxs-lookup"><span data-stu-id="29651-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="29651-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="29651-118">PARAMETERS</span></span>

### <span data-ttu-id="29651-119">-Name</span><span class="sxs-lookup"><span data-stu-id="29651-119">-Name</span></span>
<span data-ttu-id="29651-120">Der Name der Aktivitätsprotokoll Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="29651-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29651-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="29651-121">-ResourceGroupName</span></span>
<span data-ttu-id="29651-122">Der Name der Ressourcengruppe, in der die Warnungs Ressource vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="29651-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29651-123">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="29651-123">-InputObject</span></span>
<span data-ttu-id="29651-124">Legt die Inputobject-Tags-Eigenschaft des Aufrufs fest, um die Eigenschaften erforderlicher Name und Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="29651-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="29651-125">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="29651-125">-ResourceId</span></span>
<span data-ttu-id="29651-126">Legt die Eigenschaft "resourcetag-Tags" des Aufrufs fest, um den erforderlichen Namen, Eigenschaften von Ressourcengruppenname zu extrahieren.</span><span class="sxs-lookup"><span data-stu-id="29651-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="29651-127">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="29651-127">-Confirm</span></span>
<span data-ttu-id="29651-128">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="29651-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="29651-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="29651-129">-DefaultProfile</span></span>
<span data-ttu-id="29651-130">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="29651-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="29651-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="29651-131">-WhatIf</span></span>
<span data-ttu-id="29651-132">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="29651-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="29651-133">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="29651-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="29651-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="29651-134">CommonParameters</span></span>
<span data-ttu-id="29651-135">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="29651-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="29651-136">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="29651-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="29651-137">Eingaben</span><span class="sxs-lookup"><span data-stu-id="29651-137">INPUTS</span></span>

## <span data-ttu-id="29651-138">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="29651-138">OUTPUTS</span></span>

### <span data-ttu-id="29651-139">Microsoft. Azure. AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="29651-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="29651-140">Notizen</span><span class="sxs-lookup"><span data-stu-id="29651-140">NOTES</span></span>

## <span data-ttu-id="29651-141">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="29651-141">RELATED LINKS</span></span>

[<span data-ttu-id="29651-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="29651-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="29651-143">Deaktivieren-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="29651-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="29651-144">Satz-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="29651-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="29651-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="29651-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="29651-146">Neu – AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="29651-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="29651-147">Neu – AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="29651-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

