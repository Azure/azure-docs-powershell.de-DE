---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/remove-azurermbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 0ae0003c4c38b7e3922694ed01f6d8f4d10a49d2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93664930"
---
# <span data-ttu-id="c9eaa-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9eaa-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="c9eaa-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c9eaa-102">SYNOPSIS</span></span>
<span data-ttu-id="c9eaa-103">Löscht einen Anwendungspaket-Datensatz und die binäre Datei.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c9eaa-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c9eaa-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c9eaa-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c9eaa-105">DESCRIPTION</span></span>
<span data-ttu-id="c9eaa-106">Das Cmdlet **Remove-AzureRmBatchApplicationPackage** löscht einen Anwendungspaket Eintrag und die Binärdatei aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="c9eaa-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c9eaa-107">EXAMPLES</span></span>

### <span data-ttu-id="c9eaa-108">Beispiel 1: Löschen eines Anwendungspakets aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="c9eaa-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="c9eaa-109">Dieser Befehl löscht Version 1,0 der Litware-Anwendung aus dem ContosoBatchGroup-Konto.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="c9eaa-110">Der Befehl löscht sowohl den paketdatensatz als auch das BLOB, das die binäre Paketdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="c9eaa-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="c9eaa-111">PARAMETERS</span></span>

### <span data-ttu-id="c9eaa-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="c9eaa-112">-AccountName</span></span>
<span data-ttu-id="c9eaa-113">Gibt den Namen des Batch Kontos an, von dem dieses Cmdlet ein Anwendungspaket löscht.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eaa-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9eaa-114">-ApplicationId</span></span>
<span data-ttu-id="c9eaa-115">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-115">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eaa-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="c9eaa-116">-ApplicationVersion</span></span>
<span data-ttu-id="c9eaa-117">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-117">Specifies the version of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c9eaa-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9eaa-118">-DefaultProfile</span></span>
<span data-ttu-id="c9eaa-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9eaa-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9eaa-120">-ResourceGroupName</span></span>
<span data-ttu-id="c9eaa-121">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="c9eaa-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9eaa-122">CommonParameters</span></span>
<span data-ttu-id="c9eaa-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9eaa-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c9eaa-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9eaa-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c9eaa-125">INPUTS</span></span>

### <span data-ttu-id="c9eaa-126">Keine</span><span class="sxs-lookup"><span data-stu-id="c9eaa-126">None</span></span>
<span data-ttu-id="c9eaa-127">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="c9eaa-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c9eaa-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c9eaa-128">OUTPUTS</span></span>

## <span data-ttu-id="c9eaa-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="c9eaa-129">NOTES</span></span>

## <span data-ttu-id="c9eaa-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c9eaa-130">RELATED LINKS</span></span>

[<span data-ttu-id="c9eaa-131">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9eaa-131">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="c9eaa-132">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9eaa-132">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c9eaa-133">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9eaa-133">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="c9eaa-134">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="c9eaa-134">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="c9eaa-135">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9eaa-135">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="c9eaa-136">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="c9eaa-136">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


