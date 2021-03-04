---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/reset-Azstoragesyncservercertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Reset-AzStorageSyncServerCertificate.md
ms.openlocfilehash: 5d93249b6bb160d2659ead144d3fabda1af8438d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101929619"
---
# <span data-ttu-id="dacd3-101">Reset-AzStorageSyncServerCertificate</span><span class="sxs-lookup"><span data-stu-id="dacd3-101">Reset-AzStorageSyncServerCertificate</span></span>

## <span data-ttu-id="dacd3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dacd3-102">SYNOPSIS</span></span>
<span data-ttu-id="dacd3-103">Wird nur zur Problembehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="dacd3-103">Use for troubleshooting only.</span></span> <span data-ttu-id="dacd3-104">Mit diesem Befehl wird das Speichersynchronisierungsserverzertifikat rollt, das zum Beschreiben der Serveridentität für den Speichersynchronisierungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dacd3-104">This command will roll the storage sync server certificate used to describe the server identity to the storage sync service.</span></span>

## <span data-ttu-id="dacd3-105">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="dacd3-105">SYNTAX</span></span>

### <span data-ttu-id="dacd3-106">StringParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="dacd3-106">StringParameterSet (Default)</span></span>
```
Reset-AzStorageSyncServerCertificate [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacd3-107">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dacd3-107">ObjectParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentObject] <PSStorageSyncService> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dacd3-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dacd3-108">ParentStringParameterSet</span></span>
```
Reset-AzStorageSyncServerCertificate [-ParentResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dacd3-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="dacd3-109">DESCRIPTION</span></span>
<span data-ttu-id="dacd3-110">Mit diesem Befehl wird das Speichersynchronisierungsserverzertifikat rollt, das zum Beschreiben der Serveridentität für den Speichersynchronisierungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="dacd3-110">This command will roll storage sync server certificate used to describe the server identity to the storage sync service.</span></span> <span data-ttu-id="dacd3-111">Dies ist für die Verwendung in Problembehandlungsszenarien gedacht.</span><span class="sxs-lookup"><span data-stu-id="dacd3-111">This is meant for to be used in troubleshooting scenarios.</span></span> <span data-ttu-id="dacd3-112">Beim Aufrufen dieses Befehls wird das Serverzertifikat ersetzt, indem der Speichersynchronisierungsdienst aktualisiert wird, für den dieser Server ebenfalls registriert ist, indem der öffentliche Teil des Schlüssels übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="dacd3-112">When calling this command, the server certificate is replaced, updating the storage sync service this server is registered with as well, by submitting the public part of the key.</span></span> <span data-ttu-id="dacd3-113">Da ein neues Zertifikat generiert wird, wird auch die Ablaufzeit dieses Zertifikats aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="dacd3-113">Since a new certificate is generated, the expiration time of this cert is also updated.</span></span> <span data-ttu-id="dacd3-114">Dieser Befehl kann auch zum Aktualisieren eines abgelaufenen Zertifikats verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dacd3-114">This command can also be used to update an expired certificate.</span></span> <span data-ttu-id="dacd3-115">Dies kann geschehen, wenn ein Server über einen längeren Zeitraum offline ist.</span><span class="sxs-lookup"><span data-stu-id="dacd3-115">This can happen if a server is offline for an extended period of time.</span></span>

## <span data-ttu-id="dacd3-116">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="dacd3-116">EXAMPLES</span></span>

### <span data-ttu-id="dacd3-117">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="dacd3-117">Example 1</span></span>
```powershell
PS C:\> Reset-AzStorageSyncServerCertificate -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="dacd3-118">Dieser Befehl rollt das Zertifikat des lokalen Servers und informiert den entsprechenden Speichersynchronisierungsdienst auf sichere Weise über die neue Identität des Servers.</span><span class="sxs-lookup"><span data-stu-id="dacd3-118">This command will roll the local server certificate and inform the corresponding storage sync service of the server's new identity, in a secure way.</span></span>

## <span data-ttu-id="dacd3-119">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dacd3-119">PARAMETERS</span></span>

### <span data-ttu-id="dacd3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dacd3-120">-DefaultProfile</span></span>
<span data-ttu-id="dacd3-121">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dacd3-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dacd3-122">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="dacd3-122">-ParentObject</span></span>
<span data-ttu-id="dacd3-123">StorageSyncService-Objekt, das normalerweise über den -Parameter übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="dacd3-123">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="dacd3-124">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="dacd3-124">-ParentResourceId</span></span>
<span data-ttu-id="dacd3-125">StorageSyncService Parent Resource Id</span><span class="sxs-lookup"><span data-stu-id="dacd3-125">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="dacd3-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="dacd3-126">-PassThru</span></span>
<span data-ttu-id="dacd3-127">Bei normaler Ausführung gibt dieses Cmdlet keinen Wert für den Erfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="dacd3-127">In normal execution, this cmdlet returns no value on success.</span></span> <span data-ttu-id="dacd3-128">Wenn Sie den Parameter PassThru angeben, schreibt das Cmdlet nach der erfolgreichen Ausführung einen Wert in die Pipeline.</span><span class="sxs-lookup"><span data-stu-id="dacd3-128">If you provide the PassThru parameter, then the cmdlet will write a value to the pipeline after successful execution.</span></span>

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

### <span data-ttu-id="dacd3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dacd3-129">-ResourceGroupName</span></span>
<span data-ttu-id="dacd3-130">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="dacd3-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="dacd3-131">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="dacd3-131">-StorageSyncServiceName</span></span>
<span data-ttu-id="dacd3-132">Name des StorageSyncService.</span><span class="sxs-lookup"><span data-stu-id="dacd3-132">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="dacd3-133">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="dacd3-133">-Confirm</span></span>
<span data-ttu-id="dacd3-134">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="dacd3-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dacd3-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dacd3-135">-WhatIf</span></span>
<span data-ttu-id="dacd3-136">Zeigt, was passieren würde, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dacd3-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dacd3-137">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dacd3-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dacd3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dacd3-138">CommonParameters</span></span>
<span data-ttu-id="dacd3-139">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dacd3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dacd3-140">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dacd3-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dacd3-141">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="dacd3-141">INPUTS</span></span>

### <span data-ttu-id="dacd3-142">System.String</span><span class="sxs-lookup"><span data-stu-id="dacd3-142">System.String</span></span>

### <span data-ttu-id="dacd3-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="dacd3-143">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="dacd3-144">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="dacd3-144">OUTPUTS</span></span>

### <span data-ttu-id="dacd3-145">System.Object</span><span class="sxs-lookup"><span data-stu-id="dacd3-145">System.Object</span></span>
## <span data-ttu-id="dacd3-146">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="dacd3-146">NOTES</span></span>

## <span data-ttu-id="dacd3-147">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="dacd3-147">RELATED LINKS</span></span>
