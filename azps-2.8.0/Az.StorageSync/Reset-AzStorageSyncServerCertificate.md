---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 8df9d0b5149ef3b22477be1f2316bf499a3b1c6a
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93823651"
---
# <span data-ttu-id="02c99-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="02c99-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="02c99-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="02c99-102">SYNOPSIS</span></span>
<span data-ttu-id="02c99-103">Nur zur Problembehandlung verwenden.</span><span class="sxs-lookup"><span data-stu-id="02c99-103">Use for troubleshooting only.</span></span> <span data-ttu-id="02c99-104">Mit diesem Befehl wird das Storage-Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="02c99-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="02c99-105">Syntax</span><span class="sxs-lookup"><span data-stu-id="02c99-105">SYNTAX</span></span>

### <span data-ttu-id="02c99-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="02c99-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c99-107">Objectparameterset</span><span class="sxs-lookup"><span data-stu-id="02c99-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02c99-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="02c99-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02c99-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="02c99-109">DESCRIPTION</span></span>
<span data-ttu-id="02c99-110">Mit diesem Befehl wird das Speicher Synchronisierungsserver-Zertifikat gerollt, mit dem die Serveridentität für den Speicher Synchronisierungsdienst beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="02c99-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="02c99-111">Dies ist für die Verwendung in Szenarien zur Problembehandlung vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="02c99-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="02c99-112">Wenn Sie diesen Befehl aufrufen, wird das Serverzertifikat ersetzt und der Speicher Synchronisierungsdienst, bei dem dieser Server registriert ist, aktualisiert, indem der öffentliche Teil des Schlüssels übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="02c99-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="02c99-113">Da ein neues Zertifikat generiert wird, wird die Ablaufzeit dieses Zertifikats ebenfalls aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="02c99-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="02c99-114">Dieser Befehl kann auch verwendet werden, um ein abgelaufenes Zertifikat zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="02c99-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="02c99-115">Dies kann geschehen, wenn ein Server über einen längeren Zeitraum offline ist.</span><span class="sxs-lookup"><span data-stu-id="02c99-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="02c99-116">Beispiele</span><span class="sxs-lookup"><span data-stu-id="02c99-116">EXAMPLES</span></span>

### <span data-ttu-id="02c99-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="02c99-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -Name "myStorageSyncServiceName"
```

<span data-ttu-id="02c99-118">Mit diesem Befehl wird das lokale Serverzertifikat gerollt und der entsprechende Speicher Synchronisierungsdienst der neuen Identität des Servers auf sichere Weise informiert.</span><span class="sxs-lookup"><span data-stu-id="02c99-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="02c99-119">Parameter</span><span class="sxs-lookup"><span data-stu-id="02c99-119">PARAMETERS</span></span>

### <span data-ttu-id="02c99-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02c99-120">-DefaultProfile</span></span>
<span data-ttu-id="02c99-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="02c99-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02c99-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="02c99-122">-ParentObject</span></span>
<span data-ttu-id="02c99-123">StorageSyncService-Objekt, normalerweise durch den Parameter übergeben.</span><span class="sxs-lookup"><span data-stu-id="02c99-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="02c99-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="02c99-124">-ParentResourceId</span></span>
<span data-ttu-id="02c99-125">StorageSyncService übergeordnete Ressourcen-ID</span><span class="sxs-lookup"><span data-stu-id="02c99-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="02c99-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02c99-126">-PassThru</span></span>
<span data-ttu-id="02c99-127">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für Success zurück.</span><span class="sxs-lookup"><span data-stu-id="02c99-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="02c99-128">Wenn Sie den passthru-Parameter angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="02c99-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="02c99-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02c99-129">-ResourceGroupName</span></span>
<span data-ttu-id="02c99-130">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="02c99-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="02c99-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="02c99-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="02c99-132">Der Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="02c99-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="02c99-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="02c99-133">-Confirm</span></span>
<span data-ttu-id="02c99-134">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="02c99-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02c99-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02c99-135">-WhatIf</span></span>
<span data-ttu-id="02c99-136">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02c99-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="02c99-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="02c99-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02c99-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02c99-138">CommonParameters</span></span>
<span data-ttu-id="02c99-139">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="02c99-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02c99-140">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02c99-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02c99-141">Eingaben</span><span class="sxs-lookup"><span data-stu-id="02c99-141">INPUTS</span></span>

### <span data-ttu-id="02c99-142">System. String</span><span class="sxs-lookup"><span data-stu-id="02c99-142">System.String</span></span>

### <span data-ttu-id="02c99-143">Microsoft. Azure. Commands. StorageSync. Models. PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="02c99-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="02c99-144">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="02c99-144">OUTPUTS</span></span>

### <span data-ttu-id="02c99-145">System. Object</span><span class="sxs-lookup"><span data-stu-id="02c99-145">System.Object</span></span>
## <span data-ttu-id="02c99-146">Notizen</span><span class="sxs-lookup"><span data-stu-id="02c99-146">NOTES</span></span>

## <span data-ttu-id="02c99-147">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="02c99-147">RELATED LINKS</span></span>
