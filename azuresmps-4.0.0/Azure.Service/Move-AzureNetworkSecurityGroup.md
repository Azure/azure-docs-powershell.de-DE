---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 27ECCBAD-0CFE-4309-B590-BB60E1872ED5
online version: ''
schema: 2.0.0
ms.openlocfilehash: 9d96f02374eb266cb9eaa3c1cc7c200a4f154043
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006449"
---
# <span data-ttu-id="c364f-101">Move-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="c364f-101">Move-AzureNetworkSecurityGroup</span></span>

## <span data-ttu-id="c364f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c364f-102">SYNOPSIS</span></span>
<span data-ttu-id="c364f-103">Migriert eine Netzwerksicherheitsgruppe zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="c364f-103">Migrates a Network Security Group to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c364f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c364f-104">SYNTAX</span></span>

### <span data-ttu-id="c364f-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c364f-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c364f-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c364f-106">AbortMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c364f-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c364f-107">CommitMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c364f-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="c364f-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureNetworkSecurityGroup [-NetworkSecurityGroupName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c364f-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c364f-109">DESCRIPTION</span></span>
<span data-ttu-id="c364f-110">Das Cmdlet **Move-AzureNetworkSecurityGroup** migriert eine Netzwerksicherheitsgruppe zu einer Ressourcengruppe im Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="c364f-110">The **Move-AzureNetworkSecurityGroup** cmdlet migrates a Network Security Group to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="c364f-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c364f-111">EXAMPLES</span></span>

### <span data-ttu-id="c364f-112">1:</span><span class="sxs-lookup"><span data-stu-id="c364f-112">1:</span></span>
```

```

## <span data-ttu-id="c364f-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="c364f-113">PARAMETERS</span></span>

### <span data-ttu-id="c364f-114">-Abort</span><span class="sxs-lookup"><span data-stu-id="c364f-114">-Abort</span></span>
<span data-ttu-id="c364f-115">Gibt an, dass dieses Cmdlet die Migration der Netzwerksicherheitsgruppe abbricht.</span><span class="sxs-lookup"><span data-stu-id="c364f-115">Indicates that this cmdlet cancels the Network Security Group migration.</span></span>

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

### <span data-ttu-id="c364f-116">-Commit</span><span class="sxs-lookup"><span data-stu-id="c364f-116">-Commit</span></span>
<span data-ttu-id="c364f-117">Gibt an, dass dieses Cmdlet die Migration der Netzwerksicherheitsgruppe startet.</span><span class="sxs-lookup"><span data-stu-id="c364f-117">Indicates that this cmdlet starts the Network Security Group migration.</span></span>

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

### <span data-ttu-id="c364f-118">-Information</span><span class="sxs-lookup"><span data-stu-id="c364f-118">-InformationAction</span></span>
<span data-ttu-id="c364f-119">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="c364f-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="c364f-120">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="c364f-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="c364f-121">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="c364f-121">Continue</span></span>
- <span data-ttu-id="c364f-122">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="c364f-122">Ignore</span></span>
- <span data-ttu-id="c364f-123">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="c364f-123">Inquire</span></span>
- <span data-ttu-id="c364f-124">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="c364f-124">SilentlyContinue</span></span>
- <span data-ttu-id="c364f-125">Beenden</span><span class="sxs-lookup"><span data-stu-id="c364f-125">Stop</span></span>
- <span data-ttu-id="c364f-126">Anhalten</span><span class="sxs-lookup"><span data-stu-id="c364f-126">Suspend</span></span>

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

### <span data-ttu-id="c364f-127">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="c364f-127">-InformationVariable</span></span>
<span data-ttu-id="c364f-128">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="c364f-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="c364f-129">-NetworkSecurityGroupName</span><span class="sxs-lookup"><span data-stu-id="c364f-129">-NetworkSecurityGroupName</span></span>
<span data-ttu-id="c364f-130">Gibt den Namen der Netzwerksicherheitsgruppe an, die dieses Cmdlet migriert.</span><span class="sxs-lookup"><span data-stu-id="c364f-130">Specifies the name of the Network Security Group that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="c364f-131">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="c364f-131">-Prepare</span></span>
<span data-ttu-id="c364f-132">Gibt an, dass dieses Cmdlet die Netzwerksicherheitsgruppe für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="c364f-132">Indicates that this cmdlet prepares the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="c364f-133">-Profil</span><span class="sxs-lookup"><span data-stu-id="c364f-133">-Profile</span></span>
<span data-ttu-id="c364f-134">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="c364f-134">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="c364f-135">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="c364f-135">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="c364f-136">-Validate</span><span class="sxs-lookup"><span data-stu-id="c364f-136">-Validate</span></span>
<span data-ttu-id="c364f-137">Gibt an, dass dieses Cmdlet die Netzwerksicherheitsgruppe für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="c364f-137">Specifies that this cmdlet validates the Network Security Group for migration.</span></span>

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

### <span data-ttu-id="c364f-138">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="c364f-138">-Confirm</span></span>
<span data-ttu-id="c364f-139">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c364f-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c364f-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c364f-140">-WhatIf</span></span>
<span data-ttu-id="c364f-141">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c364f-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c364f-142">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c364f-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c364f-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c364f-143">CommonParameters</span></span>
<span data-ttu-id="c364f-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c364f-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c364f-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c364f-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c364f-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c364f-146">INPUTS</span></span>

## <span data-ttu-id="c364f-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c364f-147">OUTPUTS</span></span>

## <span data-ttu-id="c364f-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="c364f-148">NOTES</span></span>

## <span data-ttu-id="c364f-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c364f-149">RELATED LINKS</span></span>

[<span data-ttu-id="c364f-150">Verschieben-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="c364f-150">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="c364f-151">Verschieben-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="c364f-151">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="c364f-152">Verschieben-AzureService</span><span class="sxs-lookup"><span data-stu-id="c364f-152">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="c364f-153">Verschieben-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="c364f-153">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)

[<span data-ttu-id="c364f-154">Verschieben-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="c364f-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


