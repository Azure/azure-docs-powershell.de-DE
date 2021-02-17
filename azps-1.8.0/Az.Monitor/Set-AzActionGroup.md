---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActionGroup.md
ms.openlocfilehash: b408736aa0c43597993a2407f144c976417903b8
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402897"
---
# <span data-ttu-id="9a982-101">Set-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="9a982-101">Set-AzActionGroup</span></span>

## <span data-ttu-id="9a982-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a982-102">SYNOPSIS</span></span>
<span data-ttu-id="9a982-103">Erstellt eine neue Aktionsgruppe oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-103">Creates a new or updates an existing action group.</span></span>

## <span data-ttu-id="9a982-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="9a982-104">SYNTAX</span></span>

### <span data-ttu-id="9a982-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="9a982-105">ByPropertyName (Default)</span></span>
```
Set-AzActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a982-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="9a982-106">ByResourceId</span></span>
```
Set-AzActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a982-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="9a982-107">ByInputObject</span></span>
```
Set-AzActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a982-108">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="9a982-108">DESCRIPTION</span></span>
<span data-ttu-id="9a982-109">Das **Cmdlet "Set-AzActionGroup"** erstellt eine neue Aktionsgruppe oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-109">The **Set-AzActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="9a982-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="9a982-110">EXAMPLES</span></span>

### <span data-ttu-id="9a982-111">Beispiel 1: Erstellen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="9a982-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="9a982-112">Mit den ersten beiden Befehlen werden zwei Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="9a982-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="9a982-113">Der letzte Befehl erstellt eine Aktionsgruppe, die die beiden Empfänger einschliesslich.</span><span class="sxs-lookup"><span data-stu-id="9a982-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="9a982-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a982-114">PARAMETERS</span></span>

### <span data-ttu-id="9a982-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a982-115">-DefaultProfile</span></span>
<span data-ttu-id="9a982-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9a982-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9a982-117">-DisableGroup</span><span class="sxs-lookup"><span data-stu-id="9a982-117">-DisableGroup</span></span>
<span data-ttu-id="9a982-118">Deaktiviert die Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-118">Disables the action group.</span></span>

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

### <span data-ttu-id="9a982-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9a982-119">-InputObject</span></span>
<span data-ttu-id="9a982-120">Die Aktionsgruppe "resourc"</span><span class="sxs-lookup"><span data-stu-id="9a982-120">The action group resourc</span></span>

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

### <span data-ttu-id="9a982-121">-Name</span><span class="sxs-lookup"><span data-stu-id="9a982-121">-Name</span></span>
<span data-ttu-id="9a982-122">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-122">The name of the action group.</span></span>

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

### <span data-ttu-id="9a982-123">-Receiver</span><span class="sxs-lookup"><span data-stu-id="9a982-123">-Receiver</span></span>
<span data-ttu-id="9a982-124">Die Liste der Empfänger der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-124">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="9a982-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a982-125">-ResourceGroupName</span></span>
<span data-ttu-id="9a982-126">Die Ressourcengruppe nam</span><span class="sxs-lookup"><span data-stu-id="9a982-126">The resource group nam</span></span>

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

### <span data-ttu-id="9a982-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9a982-127">-ResourceId</span></span>
<span data-ttu-id="9a982-128">Die Ressource i</span><span class="sxs-lookup"><span data-stu-id="9a982-128">The resource i</span></span>

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

### <span data-ttu-id="9a982-129">-ShortName</span><span class="sxs-lookup"><span data-stu-id="9a982-129">-ShortName</span></span>
<span data-ttu-id="9a982-130">Der kurzname der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="9a982-130">The short name of the action group.</span></span>

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

### <span data-ttu-id="9a982-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="9a982-131">-Tag</span></span>
<span data-ttu-id="9a982-132">Die Tags der Aktionsgruppe "resourc"</span><span class="sxs-lookup"><span data-stu-id="9a982-132">The tags of the action group resourc</span></span>

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

### <span data-ttu-id="9a982-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a982-133">-Confirm</span></span>
<span data-ttu-id="9a982-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="9a982-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a982-135">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="9a982-135">-WhatIf</span></span>
<span data-ttu-id="9a982-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9a982-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a982-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="9a982-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a982-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a982-138">CommonParameters</span></span>
<span data-ttu-id="9a982-139">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a982-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a982-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a982-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a982-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="9a982-141">INPUTS</span></span>

### <span data-ttu-id="9a982-142">System.String</span><span class="sxs-lookup"><span data-stu-id="9a982-142">System.String</span></span>

### <span data-ttu-id="9a982-143">System.Collections.Generic.List'1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="9a982-143">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="9a982-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="9a982-144">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="9a982-145">System.Collections.Generic.IDictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="9a982-145">System.Collections.Generic.IDictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="9a982-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9a982-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9a982-147">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="9a982-147">OUTPUTS</span></span>

### <span data-ttu-id="9a982-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="9a982-148">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="9a982-149">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="9a982-149">NOTES</span></span>

## <span data-ttu-id="9a982-150">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="9a982-150">RELATED LINKS</span></span>

<span data-ttu-id="9a982-151">[Get-AzActionGroup](./Get-AzActionGroup.md) 
 [Remove-AzActionGroup](./Remove-AzActionGroup.md)</span><span class="sxs-lookup"><span data-stu-id="9a982-151">[Get-AzActionGroup](./Get-AzActionGroup.md)
[Remove-AzActionGroup](./Remove-AzActionGroup.md)</span></span>

