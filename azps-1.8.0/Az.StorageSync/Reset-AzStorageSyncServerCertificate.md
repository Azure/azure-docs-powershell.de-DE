---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 4c27cc1cadb7d667793aa297303e539bd8db186f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93658678"
---
# <span data-ttu-id="77d9e-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="77d9e-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="77d9e-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="77d9e-102">SYNOPSIS</span></span>
<span data-ttu-id="77d9e-103">Nur zur Problembehandlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="77d9e-103">Use for troubleshooting only.</span></span> <span data-ttu-id="77d9e-104">Mit diesem Befehl wird das Storage-Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="77d9e-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="77d9e-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="77d9e-105">SYNTAX</span></span>

### <span data-ttu-id="77d9e-106">Objectparameterset (Standard)</span><span class="sxs-lookup"><span data-stu-id="77d9e-106">ObjectParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d9e-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="77d9e-107">StringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="77d9e-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="77d9e-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="77d9e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="77d9e-109">DESCRIPTION</span></span>
<span data-ttu-id="77d9e-110">Mit diesem Befehl wird das Speicher Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="77d9e-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="77d9e-111">Dies ist für die Verwendung in Szenarien zur Problembehandlung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="77d9e-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="77d9e-112">Wenn Sie diesen Befehl aufrufen, wird das Serverzertifikat ersetzt und der Speicher Synchronisierungsdienst, bei dem dieser Server registriert ist, aktualisiert, indem der öffentliche Teil des Schlüssels übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="77d9e-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="77d9e-113">Da ein neues Zertifikat generiert wird, wird die Ablaufzeit dieses Zertifikats ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="77d9e-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="77d9e-114">Dieser Befehl kann auch verwendet werden, um ein abgelaufenes Zertifikat zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="77d9e-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="77d9e-115">Dies kann geschehen, wenn ein Server über einen längeren Zeitraum offline ist.</span><span class="sxs-lookup"><span data-stu-id="77d9e-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="77d9e-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="77d9e-116">EXAMPLES</span></span>

### <span data-ttu-id="77d9e-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="77d9e-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="77d9e-118">Mit diesem Befehl wird das lokale Serverzertifikat gerollt und der entsprechende Speicher Synchronisierungsdienst der neuen Identität des Servers auf sichere Weise informiert.</span><span class="sxs-lookup"><span data-stu-id="77d9e-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="77d9e-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d9e-119">PARAMETERS</span></span>

### <span data-ttu-id="77d9e-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77d9e-120">-DefaultProfile</span></span>
<span data-ttu-id="77d9e-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="77d9e-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="77d9e-122">-ParentObject</span></span>
<span data-ttu-id="77d9e-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="77d9e-123">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="77d9e-124">-ParentResourceId</span></span>
<span data-ttu-id="77d9e-125">StorageSyncService übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="77d9e-125">StorageSyncService Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="77d9e-126">-PassThru</span></span>
<span data-ttu-id="77d9e-127">{{Fill passthru Description}}</span><span class="sxs-lookup"><span data-stu-id="77d9e-127">{{Fill PassThru Description}}</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77d9e-128">-ResourceGroupName</span></span>
<span data-ttu-id="77d9e-129">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="77d9e-129">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-130">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="77d9e-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="77d9e-131">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="77d9e-131">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="77d9e-132">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="77d9e-132">-Confirm</span></span>
<span data-ttu-id="77d9e-133">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="77d9e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="77d9e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="77d9e-134">-WhatIf</span></span>
<span data-ttu-id="77d9e-135">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="77d9e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="77d9e-136">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="77d9e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="77d9e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77d9e-137">CommonParameters</span></span>
<span data-ttu-id="77d9e-138">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77d9e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77d9e-139">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77d9e-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77d9e-140">Eingaben</span><span class="sxs-lookup"><span data-stu-id="77d9e-140">INPUTS</span></span>

### <span data-ttu-id="77d9e-141">System. String</span><span class="sxs-lookup"><span data-stu-id="77d9e-141">System.String</span></span>

### <span data-ttu-id="77d9e-142">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="77d9e-142">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="77d9e-143">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="77d9e-143">OUTPUTS</span></span>

### <span data-ttu-id="77d9e-144">System. Object</span><span class="sxs-lookup"><span data-stu-id="77d9e-144">System.Object</span></span>
## <span data-ttu-id="77d9e-145">Notizen</span><span class="sxs-lookup"><span data-stu-id="77d9e-145">NOTES</span></span>

## <span data-ttu-id="77d9e-146">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="77d9e-146">RELATED LINKS</span></span>
