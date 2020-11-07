---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchpoolosversion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchPoolOSVersion.md
ms.openlocfilehash: f35238b6236764cc3ea75132064aede71f715458
ms.sourcegitcommit: b72b338525ee302597b3a54a11453f4881d22689
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/13/2020
ms.locfileid: "93847756"
---
# <span data-ttu-id="37b2f-101">Set-AzBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="37b2f-101">Set-AzBatchPoolOSVersion</span></span>

## <span data-ttu-id="37b2f-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="37b2f-102">SYNOPSIS</span></span>
<span data-ttu-id="37b2f-103">Ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="37b2f-103">Changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="37b2f-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="37b2f-104">SYNTAX</span></span>

```
Set-AzBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="37b2f-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="37b2f-105">DESCRIPTION</span></span>
<span data-ttu-id="37b2f-106">Das Cmdlet " **Satz-AzBatchPoolOSVersion** " ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="37b2f-106">The **Set-AzBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="37b2f-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="37b2f-107">EXAMPLES</span></span>

### <span data-ttu-id="37b2f-108">Beispiel 1: Einrichten der Zielbetriebssystem-Version eines Pools</span><span class="sxs-lookup"><span data-stu-id="37b2f-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="37b2f-109">Mit diesem Befehl wird die Zielbetriebssystem-Version des Pools MyPool auf WA-Guest-OS-4.20 _201505-01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="37b2f-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="37b2f-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="37b2f-110">PARAMETERS</span></span>

### <span data-ttu-id="37b2f-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="37b2f-111">-BatchContext</span></span>
<span data-ttu-id="37b2f-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b2f-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="37b2f-113">Wenn Sie das Get-AzBatchAccount-Cmdlet zum Abrufen Ihrer BatchAccountContext verwenden, wird bei der Interaktion mit dem Batch Dienst die Azure Active Directory-Authentifizierung verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b2f-113">If you use the Get-AzBatchAccount cmdlet to get your BatchAccountContext, then Azure Active Directory authentication will be used when interacting with the Batch service.</span></span> <span data-ttu-id="37b2f-114">Wenn Sie stattdessen die Authentifizierung mit freigegebenen Schlüsseln verwenden möchten, verwenden Sie das Get-AzBatchAccountKeys-Cmdlet, um ein BatchAccountContext-Objekt mit ausgefüllten Zugriffstasten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="37b2f-114">To use shared key authentication instead, use the Get-AzBatchAccountKeys cmdlet to get a BatchAccountContext object with its access keys populated.</span></span> <span data-ttu-id="37b2f-115">Bei Verwendung der Authentifizierung mit freigegebenen Schlüsseln wird standardmäßig die primäre Zugriffstaste verwendet.</span><span class="sxs-lookup"><span data-stu-id="37b2f-115">When using shared key authentication, the primary access key is used by default.</span></span> <span data-ttu-id="37b2f-116">Wenn Sie den zu verwendenden Schlüssel ändern möchten, müssen Sie die BatchAccountContext. KeyInUse-Eigenschaft festlegen.</span><span class="sxs-lookup"><span data-stu-id="37b2f-116">To change the key to use, set the BatchAccountContext.KeyInUse property.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Batch.BatchAccountContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b2f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="37b2f-117">-DefaultProfile</span></span>
<span data-ttu-id="37b2f-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="37b2f-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="37b2f-119">-ID</span><span class="sxs-lookup"><span data-stu-id="37b2f-119">-Id</span></span>
<span data-ttu-id="37b2f-120">Gibt die ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="37b2f-120">Specifies the ID of the pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="37b2f-121">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="37b2f-121">-TargetOSVersion</span></span>
<span data-ttu-id="37b2f-122">Gibt die Azure Guest-Betriebssystemversion an, die auf den virtuellen Computern im Pool installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="37b2f-122">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="37b2f-123">Weitere Informationen zu Azure Guest-Betriebssystemversionen finden Sie unter Azure Guest OS Releases und SDK Compatibility Matrix https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="37b2f-123">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37b2f-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37b2f-124">CommonParameters</span></span>
<span data-ttu-id="37b2f-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="37b2f-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37b2f-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37b2f-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37b2f-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="37b2f-127">INPUTS</span></span>

### <span data-ttu-id="37b2f-128">System. String</span><span class="sxs-lookup"><span data-stu-id="37b2f-128">System.String</span></span>

### <span data-ttu-id="37b2f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="37b2f-129">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="37b2f-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="37b2f-130">OUTPUTS</span></span>

### <span data-ttu-id="37b2f-131">System. void</span><span class="sxs-lookup"><span data-stu-id="37b2f-131">System.Void</span></span>

## <span data-ttu-id="37b2f-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="37b2f-132">NOTES</span></span>

## <span data-ttu-id="37b2f-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="37b2f-133">RELATED LINKS</span></span>

[<span data-ttu-id="37b2f-134">Get-AzBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="37b2f-134">Get-AzBatchAccountKeys</span></span>](./Get-AzBatchAccountKey.md)


