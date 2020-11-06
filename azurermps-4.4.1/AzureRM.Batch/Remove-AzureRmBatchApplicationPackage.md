---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Remove-AzureRmBatchApplicationPackage.md
ms.openlocfilehash: 8ef7ba1c678c09ba10bd87c301a417600f51fe0c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93499210"
---
# <span data-ttu-id="ac142-101">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac142-101">Remove-AzureRmBatchApplicationPackage</span></span>

## <span data-ttu-id="ac142-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ac142-102">SYNOPSIS</span></span>
<span data-ttu-id="ac142-103">Löscht einen Anwendungspaket-Datensatz und die binäre Datei.</span><span class="sxs-lookup"><span data-stu-id="ac142-103">Deletes an application package record and the binary file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ac142-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ac142-104">SYNTAX</span></span>

```
Remove-AzureRmBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ac142-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ac142-105">DESCRIPTION</span></span>
<span data-ttu-id="ac142-106">Das Cmdlet **Remove-AzureRmBatchApplicationPackage** löscht einen Anwendungspaket Eintrag und die Binärdatei aus einem Azure-Batch Konto.</span><span class="sxs-lookup"><span data-stu-id="ac142-106">The **Remove-AzureRmBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="ac142-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ac142-107">EXAMPLES</span></span>

### <span data-ttu-id="ac142-108">Beispiel 1: Löschen eines Anwendungspakets aus einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="ac142-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzureRmBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="ac142-109">Dieser Befehl löscht Version 1,0 der Litware-Anwendung aus dem ContosoBatchGroup-Konto.</span><span class="sxs-lookup"><span data-stu-id="ac142-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="ac142-110">Der Befehl löscht sowohl den paketdatensatz als auch das BLOB, das die binäre Paketdatei enthält.</span><span class="sxs-lookup"><span data-stu-id="ac142-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="ac142-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ac142-111">PARAMETERS</span></span>

### <span data-ttu-id="ac142-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ac142-112">-AccountName</span></span>
<span data-ttu-id="ac142-113">Gibt den Namen des Batch Kontos an, von dem dieses Cmdlet ein Anwendungspaket löscht.</span><span class="sxs-lookup"><span data-stu-id="ac142-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac142-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ac142-114">-ApplicationId</span></span>
<span data-ttu-id="ac142-115">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ac142-115">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac142-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="ac142-116">-ApplicationVersion</span></span>
<span data-ttu-id="ac142-117">Gibt die Version der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ac142-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac142-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ac142-118">-ResourceGroupName</span></span>
<span data-ttu-id="ac142-119">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="ac142-119">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ac142-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ac142-120">-DefaultProfile</span></span>
<span data-ttu-id="ac142-121">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ac142-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ac142-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ac142-122">CommonParameters</span></span>
<span data-ttu-id="ac142-123">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ac142-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ac142-124">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ac142-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ac142-125">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ac142-125">INPUTS</span></span>

## <span data-ttu-id="ac142-126">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ac142-126">OUTPUTS</span></span>

## <span data-ttu-id="ac142-127">Notizen</span><span class="sxs-lookup"><span data-stu-id="ac142-127">NOTES</span></span>

## <span data-ttu-id="ac142-128">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ac142-128">RELATED LINKS</span></span>

[<span data-ttu-id="ac142-129">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac142-129">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="ac142-130">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac142-130">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ac142-131">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac142-131">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ac142-132">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ac142-132">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ac142-133">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac142-133">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ac142-134">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ac142-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


