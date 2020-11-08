---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 2B0CC65A-0A73-4FFE-BF7C-B148871909D9
online version: ''
schema: 2.0.0
ms.openlocfilehash: df768878bf26c186751171edf7ed41acb3f7d15a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006444"
---
# <span data-ttu-id="572c2-101">Move-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="572c2-101">Move-AzureVirtualNetwork</span></span>

## <span data-ttu-id="572c2-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="572c2-102">SYNOPSIS</span></span>
<span data-ttu-id="572c2-103">Migriert ein virtuelles Netzwerk zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="572c2-103">Migrates a virtual network to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="572c2-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="572c2-104">SYNTAX</span></span>

### <span data-ttu-id="572c2-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="572c2-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Validate] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="572c2-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="572c2-106">AbortMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Abort] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="572c2-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="572c2-107">CommitMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Commit] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="572c2-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="572c2-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureVirtualNetwork [-VirtualNetworkName] <String> [-Prepare] [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="572c2-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="572c2-109">DESCRIPTION</span></span>
<span data-ttu-id="572c2-110">Das Cmdlet **Move-AzureVirtualNetwork** migriert ein virtuelles Netzwerk zu einer Ressourcengruppe im Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="572c2-110">The **Move-AzureVirtualNetwork** cmdlet migrates a virtual network to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="572c2-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="572c2-111">EXAMPLES</span></span>

### <span data-ttu-id="572c2-112">Beispiel 1: Vorbereiten der Migration virtueller Netzwerke</span><span class="sxs-lookup"><span data-stu-id="572c2-112">Example 1: Prepare virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Prepare -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="572c2-113">Dieser Befehl bereitet das virtuelle Netzwerk mit dem Namen "ContosoVNET" für die Migration auf den Azure Resource Manager-Stapel vor.</span><span class="sxs-lookup"><span data-stu-id="572c2-113">This command prepares the virtual network named ContosoVNET for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="572c2-114">Beispiel 2: Starten der Migration virtueller Netzwerke</span><span class="sxs-lookup"><span data-stu-id="572c2-114">Example 2: Start virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Commit -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="572c2-115">Mit diesem Befehl wird die Migration des virtuellen Netzwerks mit dem Namen ContosoVNET zum Azure Resource Manager-Stapel gestartet.</span><span class="sxs-lookup"><span data-stu-id="572c2-115">This command starts migration of the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="572c2-116">Beispiel 3: Überprüfen der Migration virtueller Netzwerke</span><span class="sxs-lookup"><span data-stu-id="572c2-116">Example 3: Validate virtual network migration</span></span>
```
PS C:\> Move-AzureVirtualNetwork -Validate -VirtualNetworkName "ContosoVNET"
```

<span data-ttu-id="572c2-117">Mit diesem Befehl wird die Migration für das virtuelle Netzwerk mit dem Namen ContosoVNET zum Azure Resource Manager-Stapel überprüft.</span><span class="sxs-lookup"><span data-stu-id="572c2-117">This command validates migration for the virtual network named ContosoVNET to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="572c2-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="572c2-118">PARAMETERS</span></span>

### <span data-ttu-id="572c2-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="572c2-119">-Abort</span></span>
<span data-ttu-id="572c2-120">Gibt an, dass dieses Cmdlet die Migration des virtuellen Netzwerks abbricht.</span><span class="sxs-lookup"><span data-stu-id="572c2-120">Indicates that this cmdlet cancels the virtual network migration.</span></span>

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

### <span data-ttu-id="572c2-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="572c2-121">-Commit</span></span>
<span data-ttu-id="572c2-122">Gibt an, dass dieses Cmdlet die Migration des virtuellen Netzwerks startet.</span><span class="sxs-lookup"><span data-stu-id="572c2-122">Indicates that this cmdlet starts the virtual network migration.</span></span>

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

### <span data-ttu-id="572c2-123">-Information</span><span class="sxs-lookup"><span data-stu-id="572c2-123">-InformationAction</span></span>
<span data-ttu-id="572c2-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="572c2-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="572c2-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="572c2-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="572c2-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="572c2-126">Continue</span></span>
- <span data-ttu-id="572c2-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="572c2-127">Ignore</span></span>
- <span data-ttu-id="572c2-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="572c2-128">Inquire</span></span>
- <span data-ttu-id="572c2-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="572c2-129">SilentlyContinue</span></span>
- <span data-ttu-id="572c2-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="572c2-130">Stop</span></span>
- <span data-ttu-id="572c2-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="572c2-131">Suspend</span></span>

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

### <span data-ttu-id="572c2-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="572c2-132">-InformationVariable</span></span>
<span data-ttu-id="572c2-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="572c2-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="572c2-134">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="572c2-134">-Prepare</span></span>
<span data-ttu-id="572c2-135">Gibt an, dass dieses Cmdlet das virtuelle Netzwerk für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="572c2-135">Indicates that this cmdlet prepares the virtual network for migration.</span></span>

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

### <span data-ttu-id="572c2-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="572c2-136">-Profile</span></span>
<span data-ttu-id="572c2-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="572c2-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="572c2-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="572c2-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="572c2-139">-Validate</span><span class="sxs-lookup"><span data-stu-id="572c2-139">-Validate</span></span>
<span data-ttu-id="572c2-140">Gibt an, dass dieses Cmdlet das virtuelle Netzwerk für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="572c2-140">Specifies that this cmdlet validates the virtual network for migration.</span></span>

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

### <span data-ttu-id="572c2-141">-VirtualNetworkName</span><span class="sxs-lookup"><span data-stu-id="572c2-141">-VirtualNetworkName</span></span>
<span data-ttu-id="572c2-142">Name des zu migrierenden virtuellen Netzwerks</span><span class="sxs-lookup"><span data-stu-id="572c2-142">Name of the Virtual Network to migrate</span></span>

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

### <span data-ttu-id="572c2-143">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="572c2-143">-Confirm</span></span>
<span data-ttu-id="572c2-144">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="572c2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="572c2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="572c2-145">-WhatIf</span></span>
<span data-ttu-id="572c2-146">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="572c2-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="572c2-147">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="572c2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="572c2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="572c2-148">CommonParameters</span></span>
<span data-ttu-id="572c2-149">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="572c2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="572c2-150">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="572c2-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="572c2-151">Eingaben</span><span class="sxs-lookup"><span data-stu-id="572c2-151">INPUTS</span></span>

## <span data-ttu-id="572c2-152">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="572c2-152">OUTPUTS</span></span>

## <span data-ttu-id="572c2-153">Notizen</span><span class="sxs-lookup"><span data-stu-id="572c2-153">NOTES</span></span>

## <span data-ttu-id="572c2-154">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="572c2-154">RELATED LINKS</span></span>

[<span data-ttu-id="572c2-155">Verschieben-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="572c2-155">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="572c2-156">Verschieben-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="572c2-156">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="572c2-157">Verschieben-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="572c2-157">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="572c2-158">Verschieben-AzureService</span><span class="sxs-lookup"><span data-stu-id="572c2-158">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="572c2-159">Verschieben-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="572c2-159">Move-AzureStorageAccount</span></span>](./Move-AzureStorageAccount.md)


