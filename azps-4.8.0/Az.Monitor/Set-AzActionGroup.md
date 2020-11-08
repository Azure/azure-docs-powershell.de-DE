---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b10aad8cdf480dd567b0646fb3befa95fb32bf72
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94166325"
---
# <span data-ttu-id="35326-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="35326-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="35326-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="35326-102">SYNOPSIS</span></span>
<span data-ttu-id="35326-103">Erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="35326-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="35326-104">SYNTAX</span></span>

### <span data-ttu-id="35326-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="35326-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35326-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="35326-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="35326-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="35326-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="35326-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="35326-108">DESCRIPTION</span></span>
<span data-ttu-id="35326-109">Das Cmdlet " **Satz-AzActionGroup** " erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="35326-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="35326-110">EXAMPLES</span></span>

### <span data-ttu-id="35326-111">Beispiel 1: Erstellen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="35326-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="35326-112">Mit den ersten beiden Befehlen werden zwei Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="35326-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="35326-113">Der endgültige Befehl erstellt eine Aktionsgruppe, die die beiden Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="35326-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="35326-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="35326-114">PARAMETERS</span></span>

### <span data-ttu-id="35326-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="35326-115">-DefaultProfile</span></span>
<span data-ttu-id="35326-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="35326-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="35326-117">-Disablegroup</span><span class="sxs-lookup"><span data-stu-id="35326-117">-DisableGroup</span></span>
<span data-ttu-id="35326-118">Deaktiviert die Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-118">Disables the action group.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="35326-119">-InputObject</span></span>
<span data-ttu-id="35326-120">Die Ressource der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="35326-120">The action group resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-121">-Name</span><span class="sxs-lookup"><span data-stu-id="35326-121">-Name</span></span>
<span data-ttu-id="35326-122">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-122">The name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="35326-123">-Receiver</span></span>
<span data-ttu-id="35326-124">Die Liste der Empfänger der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-124">The list of receivers of the action group.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="35326-125">-ResourceGroupName</span></span>
<span data-ttu-id="35326-126">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="35326-126">The resource group nam</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="35326-127">-ResourceId</span></span>
<span data-ttu-id="35326-128">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="35326-128">The resource i</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="35326-129">-ShortName</span></span>
<span data-ttu-id="35326-130">Der kurze Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="35326-130">The short name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="35326-131">-Tag</span></span>
<span data-ttu-id="35326-132">Die Tags der Aktionsgruppen Ressource</span><span class="sxs-lookup"><span data-stu-id="35326-132">The tags of the action group resource</span></span>

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByPropertyName, ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.IDictionary`2[System.String,System.String]
Parameter Sets: ByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="35326-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="35326-133">-Confirm</span></span>
<span data-ttu-id="35326-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="35326-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="35326-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="35326-135">-WhatIf</span></span>
<span data-ttu-id="35326-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="35326-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="35326-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="35326-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="35326-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="35326-138">CommonParameters</span></span>
<span data-ttu-id="35326-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="35326-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="35326-140">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="35326-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="35326-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="35326-141">INPUTS</span></span>

### <span data-ttu-id="35326-142">System. String</span><span class="sxs-lookup"><span data-stu-id="35326-142">System.String</span></span>

### <span data-ttu-id="35326-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. PowerShell. Cmdlets. Monitor, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="35326-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="35326-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="35326-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="35326-145">System. Collections. Generic. IDictionary ' 2 [[System. String, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e], [System. String, System. private. CoreLib, Version = 4.0.0.0, Kultur = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="35326-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="35326-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="35326-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="35326-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="35326-147">OUTPUTS</span></span>

### <span data-ttu-id="35326-148">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="35326-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="35326-149">Notizen</span><span class="sxs-lookup"><span data-stu-id="35326-149">NOTES</span></span>

## <span data-ttu-id="35326-150">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="35326-150">RELATED LINKS</span></span>

<span data-ttu-id="35326-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md) 
 [Neu – AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="35326-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)
[New-AzActionGroupReceiver](./New-AzActionGroupReceiver.md)</span></span>
