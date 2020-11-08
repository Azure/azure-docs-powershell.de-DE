---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6AFD3971-460D-4F6A-B266-6ED98DC81CD4
online version: ''
schema: 2.0.0
ms.openlocfilehash: c007e3a318067f29da6ea710c25cf2c52d5df2b4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/18/2020
ms.locfileid: "94006445"
---
# <span data-ttu-id="81a58-101">Move-AzureStorageAccount</span><span class="sxs-lookup"><span data-stu-id="81a58-101">Move-AzureStorageAccount</span></span>

## <span data-ttu-id="81a58-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="81a58-102">SYNOPSIS</span></span>
<span data-ttu-id="81a58-103">Migriert ein Speicherkonto zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="81a58-103">Migrates a storage account to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="81a58-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="81a58-104">SYNTAX</span></span>

### <span data-ttu-id="81a58-105">ValidateMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a58-105">ValidateMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Validate] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="81a58-106">AbortMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a58-106">AbortMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Abort] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="81a58-107">CommitMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a58-107">CommitMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Commit] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="81a58-108">PrepareMigrationParameterSet</span><span class="sxs-lookup"><span data-stu-id="81a58-108">PrepareMigrationParameterSet</span></span>
```
Move-AzureStorageAccount [-Prepare] [-StorageAccountName] <String> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="81a58-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="81a58-109">DESCRIPTION</span></span>
<span data-ttu-id="81a58-110">Mit dem Cmdlet **Move-AzureStorageAccount** wird ein Speicherkonto zu einer Ressourcengruppe im Azure Resource Manager-Stapel migriert.</span><span class="sxs-lookup"><span data-stu-id="81a58-110">The **Move-AzureStorageAccount** cmdlet migrates a storage account to a resource group in the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="81a58-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="81a58-111">EXAMPLES</span></span>

### <span data-ttu-id="81a58-112">Beispiel 1: Vorbereiten der Migration von Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="81a58-112">Example 1: Prepare storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Prepare -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="81a58-113">Dieser Befehl bereitet das Speicherkonto mit dem Namen "ContosoStorageName" für die Migration auf den Azure Resource Manager-Stapel vor.</span><span class="sxs-lookup"><span data-stu-id="81a58-113">This command prepares the storage account named ContosoStorageName for migration to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="81a58-114">Beispiel 2: Starten der Migration von Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="81a58-114">Example 2: Start storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Commit -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="81a58-115">Mit diesem Befehl wird die Migration des speicherkontos mit dem Namen ContosoStorageName in den Azure Resource Manager-Stapel gestartet.</span><span class="sxs-lookup"><span data-stu-id="81a58-115">This command starts migration of the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

### <span data-ttu-id="81a58-116">Beispiel 3: Überprüfen der Migration von Speicherkonten</span><span class="sxs-lookup"><span data-stu-id="81a58-116">Example 3: Validate storage account migration</span></span>
```
PS C:\> Move-AzureStorageAccount -Validate -StorageAccountName "ContosoStorageName"
```

<span data-ttu-id="81a58-117">Dieser Befehl überprüft die Migration für das Speicherkonto mit dem Namen ContosoStorageName zum Azure Resource Manager-Stapel.</span><span class="sxs-lookup"><span data-stu-id="81a58-117">This command validates migration for the storage account named ContosoStorageName to the Azure Resource Manager stack.</span></span>

## <span data-ttu-id="81a58-118">Parameter</span><span class="sxs-lookup"><span data-stu-id="81a58-118">PARAMETERS</span></span>

### <span data-ttu-id="81a58-119">-Abort</span><span class="sxs-lookup"><span data-stu-id="81a58-119">-Abort</span></span>
<span data-ttu-id="81a58-120">Gibt an, dass dieses Cmdlet die Migration des speicherkontos abbricht.</span><span class="sxs-lookup"><span data-stu-id="81a58-120">Indicates that this cmdlet cancels the storage account migration.</span></span>

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

### <span data-ttu-id="81a58-121">-Commit</span><span class="sxs-lookup"><span data-stu-id="81a58-121">-Commit</span></span>
<span data-ttu-id="81a58-122">Gibt an, dass dieses Cmdlet die Migration des speicherkontos startet.</span><span class="sxs-lookup"><span data-stu-id="81a58-122">Indicates that this cmdlet starts the storage account migration.</span></span>

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

### <span data-ttu-id="81a58-123">-Information</span><span class="sxs-lookup"><span data-stu-id="81a58-123">-InformationAction</span></span>
<span data-ttu-id="81a58-124">Gibt an, wie dieses Cmdlet auf ein Informationsereignis reagiert.</span><span class="sxs-lookup"><span data-stu-id="81a58-124">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="81a58-125">Die zulässigen Werte für diesen Parameter lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="81a58-125">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="81a58-126">Weiterhin</span><span class="sxs-lookup"><span data-stu-id="81a58-126">Continue</span></span>
- <span data-ttu-id="81a58-127">Ignorieren</span><span class="sxs-lookup"><span data-stu-id="81a58-127">Ignore</span></span>
- <span data-ttu-id="81a58-128">Erkundigen</span><span class="sxs-lookup"><span data-stu-id="81a58-128">Inquire</span></span>
- <span data-ttu-id="81a58-129">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="81a58-129">SilentlyContinue</span></span>
- <span data-ttu-id="81a58-130">Beenden</span><span class="sxs-lookup"><span data-stu-id="81a58-130">Stop</span></span>
- <span data-ttu-id="81a58-131">Anhalten</span><span class="sxs-lookup"><span data-stu-id="81a58-131">Suspend</span></span>

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

### <span data-ttu-id="81a58-132">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="81a58-132">-InformationVariable</span></span>
<span data-ttu-id="81a58-133">Gibt eine Informations Variable an.</span><span class="sxs-lookup"><span data-stu-id="81a58-133">Specifies an information variable.</span></span>

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

### <span data-ttu-id="81a58-134">-Vorbereiten</span><span class="sxs-lookup"><span data-stu-id="81a58-134">-Prepare</span></span>
<span data-ttu-id="81a58-135">Gibt an, dass dieses Cmdlet das Speicherkonto für die Migration vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="81a58-135">Indicates that this cmdlet prepares the storage account for migration.</span></span>

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

### <span data-ttu-id="81a58-136">-Profil</span><span class="sxs-lookup"><span data-stu-id="81a58-136">-Profile</span></span>
<span data-ttu-id="81a58-137">Gibt das Azure-Profil an, von dem dieses Cmdlet liest.</span><span class="sxs-lookup"><span data-stu-id="81a58-137">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81a58-138">Wenn Sie kein Profil angeben, liest dieses Cmdlet aus dem lokalen Standardprofil.</span><span class="sxs-lookup"><span data-stu-id="81a58-138">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81a58-139">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="81a58-139">-StorageAccountName</span></span>
<span data-ttu-id="81a58-140">Gibt den Namen des speicherkontos an, das dieses Cmdlet migriert.</span><span class="sxs-lookup"><span data-stu-id="81a58-140">Specifies the name of the storage account that this cmdlet migrates.</span></span>

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

### <span data-ttu-id="81a58-141">-Validate</span><span class="sxs-lookup"><span data-stu-id="81a58-141">-Validate</span></span>
<span data-ttu-id="81a58-142">Gibt an, dass dieses Cmdlet das Speicherkonto für die Migration überprüft.</span><span class="sxs-lookup"><span data-stu-id="81a58-142">Specifies that this cmdlet validates the storage account for migration.</span></span>

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

### <span data-ttu-id="81a58-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81a58-143">CommonParameters</span></span>
<span data-ttu-id="81a58-144">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="81a58-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81a58-145">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81a58-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81a58-146">Eingaben</span><span class="sxs-lookup"><span data-stu-id="81a58-146">INPUTS</span></span>

## <span data-ttu-id="81a58-147">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="81a58-147">OUTPUTS</span></span>

## <span data-ttu-id="81a58-148">Notizen</span><span class="sxs-lookup"><span data-stu-id="81a58-148">NOTES</span></span>

## <span data-ttu-id="81a58-149">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="81a58-149">RELATED LINKS</span></span>

[<span data-ttu-id="81a58-150">Verschieben-AzureNetworkSecurityGroup</span><span class="sxs-lookup"><span data-stu-id="81a58-150">Move-AzureNetworkSecurityGroup</span></span>](./Move-AzureNetworkSecurityGroup.md)

[<span data-ttu-id="81a58-151">Verschieben-AzureReservedIP</span><span class="sxs-lookup"><span data-stu-id="81a58-151">Move-AzureReservedIP</span></span>](./Move-AzureReservedIP.md)

[<span data-ttu-id="81a58-152">Verschieben-AzureRouteTable</span><span class="sxs-lookup"><span data-stu-id="81a58-152">Move-AzureRouteTable</span></span>](./Move-AzureRouteTable.md)

[<span data-ttu-id="81a58-153">Verschieben-AzureService</span><span class="sxs-lookup"><span data-stu-id="81a58-153">Move-AzureService</span></span>](./Move-AzureService.md)

[<span data-ttu-id="81a58-154">Verschieben-AzureVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="81a58-154">Move-AzureVirtualNetwork</span></span>](./Move-AzureVirtualNetwork.md)


