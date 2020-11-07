---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/set-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: 3f8b3ad20e9a80344227a28dd7cd1f2763cbaab4
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/15/2020
ms.locfileid: "93848488"
---
# <span data-ttu-id="7ad88-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="7ad88-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="7ad88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7ad88-102">SYNOPSIS</span></span>
<span data-ttu-id="7ad88-103">Erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7ad88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7ad88-104">SYNTAX</span></span>

### <span data-ttu-id="7ad88-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="7ad88-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ad88-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="7ad88-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7ad88-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7ad88-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7ad88-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ad88-108">DESCRIPTION</span></span>
<span data-ttu-id="7ad88-109">Das Cmdlet " **Satz-AzureRmActionGroup** " erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="7ad88-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7ad88-110">EXAMPLES</span></span>

### <span data-ttu-id="7ad88-111">Beispiel 1: Erstellen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="7ad88-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="7ad88-112">Mit den ersten beiden Befehlen werden zwei Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="7ad88-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="7ad88-113">Der endgültige Befehl erstellt eine Aktionsgruppe, die die beiden Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="7ad88-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="7ad88-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="7ad88-114">PARAMETERS</span></span>

### <span data-ttu-id="7ad88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ad88-115">-DefaultProfile</span></span>
<span data-ttu-id="7ad88-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="7ad88-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7ad88-117">-Disablegroup</span><span class="sxs-lookup"><span data-stu-id="7ad88-117">-DisableGroup</span></span>
<span data-ttu-id="7ad88-118">Deaktiviert die Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-118">Disables the action group.</span></span>

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

### <span data-ttu-id="7ad88-119">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="7ad88-119">-InputObject</span></span>
<span data-ttu-id="7ad88-120">Aktionsgruppe resourc</span><span class="sxs-lookup"><span data-stu-id="7ad88-120">The action group resourc</span></span>

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

### <span data-ttu-id="7ad88-121">-Name</span><span class="sxs-lookup"><span data-stu-id="7ad88-121">-Name</span></span>
<span data-ttu-id="7ad88-122">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-122">The name of the action group.</span></span>

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

### <span data-ttu-id="7ad88-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="7ad88-123">-Receiver</span></span>
<span data-ttu-id="7ad88-124">Die Liste der Empfänger der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="7ad88-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ad88-125">-ResourceGroupName</span></span>
<span data-ttu-id="7ad88-126">Die Ressourcengruppe Nam</span><span class="sxs-lookup"><span data-stu-id="7ad88-126">The resource group nam</span></span>

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

### <span data-ttu-id="7ad88-127">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="7ad88-127">-ResourceId</span></span>
<span data-ttu-id="7ad88-128">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="7ad88-128">The resource i</span></span>

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

### <span data-ttu-id="7ad88-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="7ad88-129">-ShortName</span></span>
<span data-ttu-id="7ad88-130">Der kurze Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7ad88-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="7ad88-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="7ad88-131">-Tag</span></span>
<span data-ttu-id="7ad88-132">Die Tags der Aktionsgruppe resourc</span><span class="sxs-lookup"><span data-stu-id="7ad88-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="7ad88-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="7ad88-133">-Confirm</span></span>
<span data-ttu-id="7ad88-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="7ad88-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7ad88-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7ad88-135">-WhatIf</span></span>
<span data-ttu-id="7ad88-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7ad88-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7ad88-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ad88-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7ad88-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ad88-138">CommonParameters</span></span>
<span data-ttu-id="7ad88-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7ad88-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ad88-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7ad88-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ad88-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7ad88-141">INPUTS</span></span>

### <span data-ttu-id="7ad88-142">System. String</span><span class="sxs-lookup"><span data-stu-id="7ad88-142">System.String</span></span>

### <span data-ttu-id="7ad88-143">System. Collections. Generic. List ' 1 [[Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupReceiverBase, Microsoft. Azure. Commands. Insights, Version = 5.1.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="7ad88-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="7ad88-144">System. Management. Automation. Switchparameter</span><span class="sxs-lookup"><span data-stu-id="7ad88-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="7ad88-145">System. Collections. Generic. IDictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="7ad88-145">System.Collections.Generic.IDictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="7ad88-146">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="7ad88-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>
<span data-ttu-id="7ad88-147">Parameter: Inputobject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="7ad88-147">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="7ad88-148">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7ad88-148">OUTPUTS</span></span>

### <span data-ttu-id="7ad88-149">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="7ad88-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="7ad88-150">Notizen</span><span class="sxs-lookup"><span data-stu-id="7ad88-150">NOTES</span></span>

## <span data-ttu-id="7ad88-151">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7ad88-151">RELATED LINKS</span></span>

<span data-ttu-id="7ad88-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="7ad88-152">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
