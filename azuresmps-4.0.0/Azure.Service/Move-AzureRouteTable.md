---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 01213154-DD8A-412F-A23D-5D9D09BEFA3A
online version: ''
schema: 2.0.0
ms.openlocfilehash: f0602015a63d28aecb498b0830619ea1560d6066
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006447"
---
# <span data-ttu-id="4aaf6-101">Move-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="4aaf6-101">Move-AzureRouteTable</span></span>

## <span data-ttu-id="4aaf6-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="4aaf6-102">SYNOPSIS</span></span>
<span data-ttu-id="4aaf6-103">Migriert eine Routingtabelle zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-103">Migrates a route table to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="4aaf6-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="4aaf6-104">SYNTAX</span></span>

### <span data-ttu-id="4aaf6-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaf6-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aaf6-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaf6-106">AbortMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aaf6-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaf6-107">CommitMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4aaf6-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="4aaf6-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureRouteTable [-RouteTableName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="4aaf6-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4aaf6-109">DESCRIPTION</span></span>
<span data-ttu-id="4aaf6-110">Das Cmdlet **Move-AzureRouteTable** migriert eine Routingtabelle zu einer Ressourcengruppe im Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-110">The **Move-AzureRouteTable** cmdlet migrates a route table to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="4aaf6-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4aaf6-111">EXAMPLES</span></span>

### <span data-ttu-id="4aaf6-112">1:</span><span class="sxs-lookup"><span data-stu-id="4aaf6-112">1:</span></span>
```

```

## <span data-ttu-id="4aaf6-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="4aaf6-113">PARAMETERS</span></span>

### <span data-ttu-id="4aaf6-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="4aaf6-114">-Abort</span></span>
<span data-ttu-id="4aaf6-115">Gibt an, dass dieses Cmdlet die Migration der Routingtabelle abbricht.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-115">Indicates that this cmdlet cancels the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AbortMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="4aaf6-116">-Commit</span></span>
<span data-ttu-id="4aaf6-117">Gibt an, dass dieses Cmdlet die Migration der Routingtabelle startet.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-117">Indicates that this cmdlet starts the route table migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: CommitMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-118">-Information</span><span class="sxs-lookup"><span data-stu-id="4aaf6-118">-InformationAction</span></span>
<span data-ttu-id="4aaf6-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="4aaf6-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="4aaf6-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="4aaf6-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="4aaf6-121">Continue</span></span>
- <span data-ttu-id="4aaf6-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="4aaf6-122">Ignore</span></span>
- <span data-ttu-id="4aaf6-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-123">Inquire</span></span>
- <span data-ttu-id="4aaf6-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="4aaf6-124">SilentlyContinue</span></span>
- <span data-ttu-id="4aaf6-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="4aaf6-125">Stop</span></span>
- <span data-ttu-id="4aaf6-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="4aaf6-126">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="4aaf6-127">-InformationVariable</span></span>
<span data-ttu-id="4aaf6-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-128">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-129">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="4aaf6-129">-Prepare</span></span>
<span data-ttu-id="4aaf6-130">Gibt an, dass dieses Cmdlet die Routingtabelle für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-130">Indicates that this cmdlet prepares the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: PrepareMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="4aaf6-131">-Profile</span></span>
<span data-ttu-id="4aaf6-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="4aaf6-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-134">-RouteTableName</span><span class="sxs-lookup"><span data-stu-id="4aaf6-134">-RouteTableName</span></span>
<span data-ttu-id="4aaf6-135">Gibt den Namen der Routingtabelle an, die von diesem Cmdlet migriert wird.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-135">Specifies the name of the route table that this cmdlet migrates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="4aaf6-136">-Validate</span></span>
<span data-ttu-id="4aaf6-137">Gibt an, dass dieses Cmdlet die Routingtabelle für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-137">Specifies that this cmdlet validates the route table for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ValidateMigrationParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-138">-Confirm</span></span>
<span data-ttu-id="4aaf6-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4aaf6-140">-WhatIf</span></span>
<span data-ttu-id="4aaf6-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4aaf6-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4aaf6-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4aaf6-143">CommonParameters</span></span>
<span data-ttu-id="4aaf6-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4aaf6-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4aaf6-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4aaf6-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4aaf6-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="4aaf6-146">INPUTS</span></span>

## <span data-ttu-id="4aaf6-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="4aaf6-147">OUTPUTS</span></span>

## <span data-ttu-id="4aaf6-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="4aaf6-148">NOTES</span></span>

## <span data-ttu-id="4aaf6-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="4aaf6-149">RELATED LINKS</span></span>

[<span data-ttu-id="4aaf6-150">Verschieben-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="4aaf6-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="4aaf6-151">Verschieben-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="4aaf6-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="4aaf6-152">Verschieben-AzureService</span><span class="sxs-lookup"><span data-stu-id="4aaf6-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="4aaf6-153">Verschieben-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="4aaf6-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="4aaf6-154">Verschieben-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4aaf6-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


