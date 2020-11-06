---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 4A6816DB-0E46-44F0-8AE9-180B1C4AAB22
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActionGroup.md
ms.openlocfilehash: 29ef822e61c13d3ea976002c465a7c114296da9f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93500841"
---
# <span data-ttu-id="92deb-101">Set-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="92deb-101">Set-AzureRmActionGroup</span></span>

## <span data-ttu-id="92deb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="92deb-102">SYNOPSIS</span></span>
<span data-ttu-id="92deb-103">Erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-103">Creates a new or updates an existing action group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="92deb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="92deb-104">SYNTAX</span></span>

### <span data-ttu-id="92deb-105">ByPropertyName (Standard)</span><span class="sxs-lookup"><span data-stu-id="92deb-105">ByPropertyName (Default)</span></span>
```
Set-AzureRmActionGroup -ResourceGroupName <String> -Name <String> -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92deb-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="92deb-106">ByResourceId</span></span>
```
Set-AzureRmActionGroup -ShortName <String>
 -Receiver <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupReceiverBase]>
 [-DisableGroup] [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="92deb-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="92deb-107">ByInputObject</span></span>
```
Set-AzureRmActionGroup [-ShortName <String>] [-DisableGroup]
 [-Tag <System.Collections.Generic.IDictionary`2[System.String,System.String]>]
 -InputObject <PSActionGroupResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="92deb-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="92deb-108">DESCRIPTION</span></span>
<span data-ttu-id="92deb-109">Das Cmdlet " **Satz-AzureRmActionGroup** " erstellt eine neue oder aktualisiert eine vorhandene Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-109">The **Set-AzureRmActionGroup** cmdlet creates a new or updates an existing action group</span></span>

## <span data-ttu-id="92deb-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="92deb-110">EXAMPLES</span></span>

### <span data-ttu-id="92deb-111">Beispiel 1: Erstellen einer Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="92deb-111">Example 1: Create an Action Group</span></span>
```
PS C:\>$email1 = New-AzureRmActionGroupReceiver -Name 'user1' -EmailReceiver -EmailAddress 'user1@example.com'
PS C:\>$sms1 = New-AzureRmActionGroupReceiver -Name 'user2' -SmsReceiver -CountryCode '1' -PhoneNumber '5555555555'
PS C:\>Set-AzureRmActionGroup -Name $actionGroupName -ResourceGroup $resourceGroupName -ShortName $shortName -Receiver $email1,$sms1
```

<span data-ttu-id="92deb-112">Mit den ersten beiden Befehlen werden zwei Empfänger erstellt.</span><span class="sxs-lookup"><span data-stu-id="92deb-112">The first two commands create two receivers.</span></span>
<span data-ttu-id="92deb-113">Der endgültige Befehl erstellt eine Aktionsgruppe, die die beiden Empfänger enthält.</span><span class="sxs-lookup"><span data-stu-id="92deb-113">The final command creates an Action Group including the two receivers.</span></span>

## <span data-ttu-id="92deb-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="92deb-114">PARAMETERS</span></span>

### <span data-ttu-id="92deb-115">-Name</span><span class="sxs-lookup"><span data-stu-id="92deb-115">-Name</span></span>
<span data-ttu-id="92deb-116">Der Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-116">The name of the action group.</span></span>

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

### <span data-ttu-id="92deb-117">-ShortName</span><span class="sxs-lookup"><span data-stu-id="92deb-117">-ShortName</span></span>
<span data-ttu-id="92deb-118">Der kurze Name der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-118">The short name of the action group.</span></span>

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

### <span data-ttu-id="92deb-119">-Receiver</span><span class="sxs-lookup"><span data-stu-id="92deb-119">-Receiver</span></span>
<span data-ttu-id="92deb-120">Die Liste der Empfänger der Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-120">The list of receivers of the action group.</span></span>

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

### <span data-ttu-id="92deb-121">-Disablegroup</span><span class="sxs-lookup"><span data-stu-id="92deb-121">-DisableGroup</span></span>
<span data-ttu-id="92deb-122">Deaktiviert die Aktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="92deb-122">Disables the action group.</span></span>

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

### <span data-ttu-id="92deb-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="92deb-123">-Confirm</span></span>
<span data-ttu-id="92deb-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="92deb-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="92deb-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="92deb-125">-DefaultProfile</span></span>
<span data-ttu-id="92deb-126">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="92deb-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="92deb-127">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="92deb-127">-InputObject</span></span>
<span data-ttu-id="92deb-128">Die Ressource der Aktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="92deb-128">The action group resource</span></span>

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

### <span data-ttu-id="92deb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="92deb-129">-ResourceGroupName</span></span>
<span data-ttu-id="92deb-130">Der Name der Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="92deb-130">The resource group name</span></span>

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

### <span data-ttu-id="92deb-131">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="92deb-131">-ResourceId</span></span>
<span data-ttu-id="92deb-132">Die Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="92deb-132">The resource id</span></span>

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

### <span data-ttu-id="92deb-133">-Tag</span><span class="sxs-lookup"><span data-stu-id="92deb-133">-Tag</span></span>
<span data-ttu-id="92deb-134">Die Tags der Aktionsgruppen Ressource</span><span class="sxs-lookup"><span data-stu-id="92deb-134">The tags of the action group resource</span></span>

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

### <span data-ttu-id="92deb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="92deb-135">-WhatIf</span></span>
<span data-ttu-id="92deb-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="92deb-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="92deb-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="92deb-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="92deb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="92deb-138">CommonParameters</span></span>
<span data-ttu-id="92deb-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="92deb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="92deb-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="92deb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="92deb-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="92deb-141">INPUTS</span></span>

## <span data-ttu-id="92deb-142">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="92deb-142">OUTPUTS</span></span>

### <span data-ttu-id="92deb-143">Microsoft. Azure. Commands. Insights. OutputClasses. PSActionGroupResource</span><span class="sxs-lookup"><span data-stu-id="92deb-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActionGroupResource</span></span>

## <span data-ttu-id="92deb-144">Notizen</span><span class="sxs-lookup"><span data-stu-id="92deb-144">NOTES</span></span>

## <span data-ttu-id="92deb-145">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="92deb-145">RELATED LINKS</span></span>

<span data-ttu-id="92deb-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md) 
 [Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md) 
 [Neu – AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span><span class="sxs-lookup"><span data-stu-id="92deb-146">[Get-AzureRmActionGroup](./Get-AzureRmActionGroup.md)
[Remove-AzureRmActionGroup](./Remove-AzureRmActionGroup.md)
[New-AzureRmActionGroupReceiver](./AzureRmActionGroupReceiver.md)</span></span>
