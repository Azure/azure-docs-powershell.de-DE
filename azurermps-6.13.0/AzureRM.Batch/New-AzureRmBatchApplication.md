---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/new-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/New-AzureRmBatchApplication.md
ms.openlocfilehash: 34c887388256e86657d1a979729333e44cb1bd77
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93480530"
---
# <span data-ttu-id="d125a-101">New-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d125a-101">New-AzureRmBatchApplication</span></span>

## <span data-ttu-id="d125a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d125a-102">SYNOPSIS</span></span>
<span data-ttu-id="d125a-103">Fügt dem angegebenen Batch Konto eine Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="d125a-103">Adds an application to the specified Batch account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d125a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d125a-104">SYNTAX</span></span>

```
New-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d125a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d125a-105">DESCRIPTION</span></span>
<span data-ttu-id="d125a-106">Mit dem Cmdlet **New-AzureRmBatchApplication** wird eine Anwendung zum angegebenen Azure-Batch Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d125a-106">The **New-AzureRmBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="d125a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d125a-107">EXAMPLES</span></span>

### <span data-ttu-id="d125a-108">Beispiel 1: Hinzufügen einer leeren Anwendung zu einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="d125a-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="d125a-109">Mit diesem Befehl wird die Litware-Anwendung im ContosoBatch-Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="d125a-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="d125a-110">Die Anwendung enthält zunächst keine Pakete.</span><span class="sxs-lookup"><span data-stu-id="d125a-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="d125a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d125a-111">PARAMETERS</span></span>

### <span data-ttu-id="d125a-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d125a-112">-AccountName</span></span>
<span data-ttu-id="d125a-113">Gibt den Namen des Batch Kontos an, dem dieses Cmdlet eine Anwendung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="d125a-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="d125a-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="d125a-114">-AllowUpdates</span></span>
<span data-ttu-id="d125a-115">Gibt an, ob Pakete in der Anwendung mit der gleichen Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="d125a-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d125a-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d125a-116">-ApplicationId</span></span>
<span data-ttu-id="d125a-117">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d125a-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d125a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d125a-118">-DefaultProfile</span></span>
<span data-ttu-id="d125a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d125a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d125a-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d125a-120">-DisplayName</span></span>
<span data-ttu-id="d125a-121">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d125a-121">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d125a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d125a-122">-ResourceGroupName</span></span>
<span data-ttu-id="d125a-123">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="d125a-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d125a-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d125a-124">CommonParameters</span></span>
<span data-ttu-id="d125a-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d125a-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d125a-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d125a-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d125a-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d125a-127">INPUTS</span></span>

### <span data-ttu-id="d125a-128">System. String</span><span class="sxs-lookup"><span data-stu-id="d125a-128">System.String</span></span>

### <span data-ttu-id="d125a-129">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d125a-129">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d125a-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d125a-130">OUTPUTS</span></span>

### <span data-ttu-id="d125a-131">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="d125a-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="d125a-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="d125a-132">NOTES</span></span>

## <span data-ttu-id="d125a-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d125a-133">RELATED LINKS</span></span>

[<span data-ttu-id="d125a-134">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d125a-134">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d125a-135">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d125a-135">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d125a-136">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d125a-136">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d125a-137">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d125a-137">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d125a-138">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d125a-138">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d125a-139">Satz-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d125a-139">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)


