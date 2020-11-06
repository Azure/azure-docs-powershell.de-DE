---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 157e7a3ee0cc7ea4a80517bf98d17c05df8c7899
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93478722"
---
# <span data-ttu-id="ad25a-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ad25a-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="ad25a-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="ad25a-102">SYNOPSIS</span></span>
<span data-ttu-id="ad25a-103">Aktualisiert die Einstellungen für die angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ad25a-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ad25a-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="ad25a-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ad25a-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ad25a-105">DESCRIPTION</span></span>
<span data-ttu-id="ad25a-106">Das Cmdlet " **Satz-AzureRmBatchApplication** " ändert die Einstellungen für die angegebene Azure-Batch Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ad25a-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="ad25a-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="ad25a-107">EXAMPLES</span></span>

### <span data-ttu-id="ad25a-108">Beispiel 1: Aktualisieren einer Anwendung in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="ad25a-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="ad25a-109">Mit diesem Befehl wird geändert, ob die Llitware-Anwendung im ContosoBatch-Konto Updates zulässt.</span><span class="sxs-lookup"><span data-stu-id="ad25a-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="ad25a-110">Der Befehl ändert nicht die Standard Version oder den Anzeigenamen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ad25a-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="ad25a-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="ad25a-111">PARAMETERS</span></span>

### <span data-ttu-id="ad25a-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="ad25a-112">-AccountName</span></span>
<span data-ttu-id="ad25a-113">Gibt den Namen des Batch Kontos an, für das dieses Cmdlet eine Anwendung ändert.</span><span class="sxs-lookup"><span data-stu-id="ad25a-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="ad25a-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="ad25a-114">-AllowUpdates</span></span>
<span data-ttu-id="ad25a-115">Gibt an, ob Pakete in der Anwendung mit der gleichen Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="ad25a-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad25a-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="ad25a-116">-ApplicationId</span></span>
<span data-ttu-id="ad25a-117">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ad25a-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="ad25a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ad25a-118">-DefaultProfile</span></span>
<span data-ttu-id="ad25a-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="ad25a-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ad25a-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="ad25a-120">-DefaultVersion</span></span>
<span data-ttu-id="ad25a-121">Gibt an, welches Paket verwendet werden soll, wenn ein Client die Anwendung anfordert, aber keine Version angibt.</span><span class="sxs-lookup"><span data-stu-id="ad25a-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad25a-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="ad25a-122">-DisplayName</span></span>
<span data-ttu-id="ad25a-123">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="ad25a-123">Specifies the display name for the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ad25a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ad25a-124">-ResourceGroupName</span></span>
<span data-ttu-id="ad25a-125">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="ad25a-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="ad25a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ad25a-126">CommonParameters</span></span>
<span data-ttu-id="ad25a-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ad25a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ad25a-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ad25a-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ad25a-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="ad25a-129">INPUTS</span></span>

### <span data-ttu-id="ad25a-130">Keine</span><span class="sxs-lookup"><span data-stu-id="ad25a-130">None</span></span>
<span data-ttu-id="ad25a-131">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="ad25a-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="ad25a-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="ad25a-132">OUTPUTS</span></span>

## <span data-ttu-id="ad25a-133">Notizen</span><span class="sxs-lookup"><span data-stu-id="ad25a-133">NOTES</span></span>

## <span data-ttu-id="ad25a-134">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="ad25a-134">RELATED LINKS</span></span>

[<span data-ttu-id="ad25a-135">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ad25a-135">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="ad25a-136">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ad25a-136">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ad25a-137">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ad25a-137">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="ad25a-138">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ad25a-138">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="ad25a-139">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="ad25a-139">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="ad25a-140">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="ad25a-140">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


