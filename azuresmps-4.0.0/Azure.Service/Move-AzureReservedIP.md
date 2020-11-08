---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: D1A4FA07-C25E-472B-9C64-695AD41274FA
online version: ''
schema: 2.0.0
ms.openlocfilehash: fb8b6a502d6abe5520cadcf776ece1f077c7d91f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006448"
---
# <span data-ttu-id="3ea99-101">Move-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="3ea99-101">Move-AzureReservedIP</span></span>

## <span data-ttu-id="3ea99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3ea99-102">SYNOPSIS</span></span>
<span data-ttu-id="3ea99-103">Migriert eine reservierte IP-Adresse zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="3ea99-103">Migrates a reserved IP address to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3ea99-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3ea99-104">SYNTAX</span></span>

### <span data-ttu-id="3ea99-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea99-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ea99-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea99-106">AbortMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ea99-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea99-107">CommitMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3ea99-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="3ea99-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureReservedIP [-ReservedIPName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3ea99-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3ea99-109">DESCRIPTION</span></span>
<span data-ttu-id="3ea99-110">Das Cmdlet **Move-AzureReservedIP** migriert eine reservierte IP-Adresse zu einer Ressourcengruppe im Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="3ea99-110">The **Move-AzureReservedIP** cmdlet migrates a reserved IP address to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="3ea99-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3ea99-111">EXAMPLES</span></span>

### <span data-ttu-id="3ea99-112">1:</span><span class="sxs-lookup"><span data-stu-id="3ea99-112">1:</span></span>
```

```

## <span data-ttu-id="3ea99-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="3ea99-113">PARAMETERS</span></span>

### <span data-ttu-id="3ea99-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="3ea99-114">-Abort</span></span>
<span data-ttu-id="3ea99-115">Gibt an, dass dieses Cmdlet die reservierte IP-Adressmigration abbricht.</span><span class="sxs-lookup"><span data-stu-id="3ea99-115">Indicates that this cmdlet cancels the reserved IP address migration.</span></span>

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

### <span data-ttu-id="3ea99-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="3ea99-116">-Commit</span></span>
<span data-ttu-id="3ea99-117">Gibt an, dass dieses Cmdlet die reservierte IP-Adressmigration startet.</span><span class="sxs-lookup"><span data-stu-id="3ea99-117">Indicates that this cmdlet starts the reserved IP address migration.</span></span>

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

### <span data-ttu-id="3ea99-118">-Information</span><span class="sxs-lookup"><span data-stu-id="3ea99-118">-InformationAction</span></span>
<span data-ttu-id="3ea99-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="3ea99-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="3ea99-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="3ea99-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="3ea99-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="3ea99-121">Continue</span></span>
- <span data-ttu-id="3ea99-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="3ea99-122">Ignore</span></span>
- <span data-ttu-id="3ea99-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="3ea99-123">Inquire</span></span>
- <span data-ttu-id="3ea99-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="3ea99-124">SilentlyContinue</span></span>
- <span data-ttu-id="3ea99-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="3ea99-125">Stop</span></span>
- <span data-ttu-id="3ea99-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="3ea99-126">Suspend</span></span>

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

### <span data-ttu-id="3ea99-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="3ea99-127">-InformationVariable</span></span>
<span data-ttu-id="3ea99-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="3ea99-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="3ea99-129">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="3ea99-129">-Prepare</span></span>
<span data-ttu-id="3ea99-130">Gibt an, dass dieses Cmdlet die reservierte IP-Adresse für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="3ea99-130">Indicates that this cmdlet prepares the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="3ea99-131">-Profil</span><span class="sxs-lookup"><span data-stu-id="3ea99-131">-Profile</span></span>
<span data-ttu-id="3ea99-132">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="3ea99-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="3ea99-133">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="3ea99-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="3ea99-134">-ReservedIPName</span><span class="sxs-lookup"><span data-stu-id="3ea99-134">-ReservedIPName</span></span>
<span data-ttu-id="3ea99-135">Gibt den Namen der reservierten IP-Adresse an, die dieses Cmdlet migriert.</span><span class="sxs-lookup"><span data-stu-id="3ea99-135">Specifies the name of the reserved IP address that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="3ea99-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="3ea99-136">-Validate</span></span>
<span data-ttu-id="3ea99-137">Gibt an, dass dieses Cmdlet die reservierte IP-Adresse für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="3ea99-137">Specifies that this cmdlet validates the reserved IP address for migration.</span></span>

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

### <span data-ttu-id="3ea99-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3ea99-138">-Confirm</span></span>
<span data-ttu-id="3ea99-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3ea99-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3ea99-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3ea99-140">-WhatIf</span></span>
<span data-ttu-id="3ea99-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ea99-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3ea99-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3ea99-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3ea99-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3ea99-143">CommonParameters</span></span>
<span data-ttu-id="3ea99-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3ea99-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3ea99-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3ea99-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3ea99-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3ea99-146">INPUTS</span></span>

## <span data-ttu-id="3ea99-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3ea99-147">OUTPUTS</span></span>

## <span data-ttu-id="3ea99-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="3ea99-148">NOTES</span></span>

## <span data-ttu-id="3ea99-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3ea99-149">RELATED LINKS</span></span>

[<span data-ttu-id="3ea99-150">Verschieben-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="3ea99-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="3ea99-151">Verschieben-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="3ea99-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="3ea99-152">Verschieben-AzureService</span><span class="sxs-lookup"><span data-stu-id="3ea99-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="3ea99-153">Verschieben-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3ea99-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="3ea99-154">Verschieben-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="3ea99-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


