---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: 4C3C6C81-7486-4ED6-BA30-2F202E654F77
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureBatchPoolOSVersion.md
ms.openlocfilehash: 23c0a68c4b517035319150caa1d4d6a3acf799cd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663612"
---
# <span data-ttu-id="45a89-101">Set-AzureBatchPoolOSVersion</span><span class="sxs-lookup"><span data-stu-id="45a89-101">Set-AzureBatchPoolOSVersion</span></span>

## <span data-ttu-id="45a89-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="45a89-102">SYNOPSIS</span></span>
<span data-ttu-id="45a89-103">Ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="45a89-103">Changes the operating system version of the specified pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45a89-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="45a89-104">SYNTAX</span></span>

```
Set-AzureBatchPoolOSVersion [-Id] <String> [-TargetOSVersion] <String> -BatchContext <BatchAccountContext>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45a89-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="45a89-105">DESCRIPTION</span></span>
<span data-ttu-id="45a89-106">Das Cmdlet " **Satz-AzureBatchPoolOSVersion** " ändert die Betriebssystemversion des angegebenen Pools.</span><span class="sxs-lookup"><span data-stu-id="45a89-106">The **Set-AzureBatchPoolOSVersion** cmdlet changes the operating system version of the specified pool.</span></span>

## <span data-ttu-id="45a89-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="45a89-107">EXAMPLES</span></span>

### <span data-ttu-id="45a89-108">Beispiel 1: Einrichten der Zielbetriebssystem-Version eines Pools</span><span class="sxs-lookup"><span data-stu-id="45a89-108">Example 1: Set the target operating system version of a pool</span></span>
```
PS C:\>Set-AzureBatchPoolOSVersion -Id "MyPool" -TargetOSVersion "WA-GUEST-OS-4.20_201505-01" -BatchContext $Context
```

<span data-ttu-id="45a89-109">Mit diesem Befehl wird die Zielbetriebssystem-Version des Pools MyPool auf WA-Guest-OS-4.20 _201505-01 festgelegt.</span><span class="sxs-lookup"><span data-stu-id="45a89-109">This command sets the target operating system version of pool MyPool to WA-GUEST-OS-4.20_201505-01.</span></span>

## <span data-ttu-id="45a89-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="45a89-110">PARAMETERS</span></span>

### <span data-ttu-id="45a89-111">-Batchcontext</span><span class="sxs-lookup"><span data-stu-id="45a89-111">-BatchContext</span></span>
<span data-ttu-id="45a89-112">Gibt die **BatchAccountContext** -Instanz an, die dieses Cmdlet für die Interaktion mit dem Batch Dienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="45a89-112">Specifies the **BatchAccountContext** instance that this cmdlet uses to interact with the Batch service.</span></span>
<span data-ttu-id="45a89-113">Wenn Sie ein **BatchAccountContext** -Objekt abrufen möchten, das Zugriffstasten für Ihr Abonnement enthält, verwenden Sie das Get-AzureRmBatchAccountKeys-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="45a89-113">To obtain a **BatchAccountContext** object that contains access keys for your subscription, use the Get-AzureRmBatchAccountKeys cmdlet.</span></span>

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

### <span data-ttu-id="45a89-114">-ID</span><span class="sxs-lookup"><span data-stu-id="45a89-114">-Id</span></span>
<span data-ttu-id="45a89-115">Gibt die ID des Pools an.</span><span class="sxs-lookup"><span data-stu-id="45a89-115">Specifies the ID of the pool.</span></span>

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

### <span data-ttu-id="45a89-116">-TargetOSVersion</span><span class="sxs-lookup"><span data-stu-id="45a89-116">-TargetOSVersion</span></span>
<span data-ttu-id="45a89-117">Gibt die Azure Guest-Betriebssystemversion an, die auf den virtuellen Computern im Pool installiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="45a89-117">Specifies the Azure Guest operating system version to install on the virtual machines in the pool.</span></span>
<span data-ttu-id="45a89-118">Weitere Informationen zu Azure Guest-Betriebssystemversionen finden Sie unter Azure Guest OS Releases und SDK Compatibility Matrix https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ ( https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/) .</span><span class="sxs-lookup"><span data-stu-id="45a89-118">For more information on Azure Guest operating system versions, see Azure Guest OS Releases and SDK Compatibility Matrixhttps://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/ (https://azure.microsoft.com/en-us/documentation/articles/cloud-services-guestos-update-matrix/).</span></span>

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

### <span data-ttu-id="45a89-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45a89-119">-DefaultProfile</span></span>
<span data-ttu-id="45a89-120">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="45a89-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45a89-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45a89-121">CommonParameters</span></span>
<span data-ttu-id="45a89-122">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45a89-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45a89-123">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45a89-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45a89-124">Eingaben</span><span class="sxs-lookup"><span data-stu-id="45a89-124">INPUTS</span></span>

### <span data-ttu-id="45a89-125">BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="45a89-125">BatchAccountContext</span></span>
<span data-ttu-id="45a89-126">Der Parameter "batchcontext" akzeptiert den Wert vom Typ "BatchAccountContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="45a89-126">Parameter 'BatchContext' accepts value of type 'BatchAccountContext' from the pipeline</span></span>

### <span data-ttu-id="45a89-127">Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="45a89-127">String</span></span>
<span data-ttu-id="45a89-128">Der Parameter "ID" akzeptiert den Wert vom Typ "Zeichenfolge" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="45a89-128">Parameter 'Id' accepts value of type 'String' from the pipeline</span></span>

## <span data-ttu-id="45a89-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="45a89-129">OUTPUTS</span></span>

## <span data-ttu-id="45a89-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="45a89-130">NOTES</span></span>

## <span data-ttu-id="45a89-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="45a89-131">RELATED LINKS</span></span>

[<span data-ttu-id="45a89-132">Get-AzureRmBatchAccountKeys</span><span class="sxs-lookup"><span data-stu-id="45a89-132">Get-AzureRmBatchAccountKeys</span></span>](./Get-AzureRmBatchAccountKeys.md)


