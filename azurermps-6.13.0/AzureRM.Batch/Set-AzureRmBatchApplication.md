---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/set-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Set-AzureRmBatchApplication.md
ms.openlocfilehash: 8ede896e6a49cee5305e7f9fd42f6dab130e7986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93498406"
---
# <span data-ttu-id="d2e73-101">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e73-101">Set-AzureRmBatchApplication</span></span>

## <span data-ttu-id="d2e73-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d2e73-102">SYNOPSIS</span></span>
<span data-ttu-id="d2e73-103">Aktualisiert die Einstellungen für die angegebene Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2e73-103">Updates settings for the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2e73-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d2e73-104">SYNTAX</span></span>

```
Set-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2e73-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d2e73-105">DESCRIPTION</span></span>
<span data-ttu-id="d2e73-106">Das Cmdlet " **Satz-AzureRmBatchApplication** " ändert die Einstellungen für die angegebene Azure-Batch Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2e73-106">The **Set-AzureRmBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="d2e73-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d2e73-107">EXAMPLES</span></span>

### <span data-ttu-id="d2e73-108">Beispiel 1: Aktualisieren einer Anwendung in einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="d2e73-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $False
```

<span data-ttu-id="d2e73-109">Mit diesem Befehl wird geändert, ob die Llitware-Anwendung im ContosoBatch-Konto Updates zulässt.</span><span class="sxs-lookup"><span data-stu-id="d2e73-109">This command changes whether the Llitware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="d2e73-110">Der Befehl ändert nicht die Standard Version oder den Anzeigenamen der Anwendung.</span><span class="sxs-lookup"><span data-stu-id="d2e73-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="d2e73-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="d2e73-111">PARAMETERS</span></span>

### <span data-ttu-id="d2e73-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="d2e73-112">-AccountName</span></span>
<span data-ttu-id="d2e73-113">Gibt den Namen des Batch Kontos an, für das dieses Cmdlet eine Anwendung ändert.</span><span class="sxs-lookup"><span data-stu-id="d2e73-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="d2e73-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="d2e73-114">-AllowUpdates</span></span>
<span data-ttu-id="d2e73-115">Gibt an, ob Pakete in der Anwendung mit der gleichen Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="d2e73-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e73-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d2e73-116">-ApplicationId</span></span>
<span data-ttu-id="d2e73-117">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d2e73-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="d2e73-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2e73-118">-DefaultProfile</span></span>
<span data-ttu-id="d2e73-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="d2e73-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2e73-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="d2e73-120">-DefaultVersion</span></span>
<span data-ttu-id="d2e73-121">Gibt an, welches Paket verwendet werden soll, wenn ein Client die Anwendung anfordert, aber keine Version angibt.</span><span class="sxs-lookup"><span data-stu-id="d2e73-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

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

### <span data-ttu-id="d2e73-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d2e73-122">-DisplayName</span></span>
<span data-ttu-id="d2e73-123">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="d2e73-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2e73-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2e73-124">-ResourceGroupName</span></span>
<span data-ttu-id="d2e73-125">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="d2e73-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="d2e73-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2e73-126">CommonParameters</span></span>
<span data-ttu-id="d2e73-127">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d2e73-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2e73-128">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2e73-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2e73-129">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d2e73-129">INPUTS</span></span>

### <span data-ttu-id="d2e73-130">System. String</span><span class="sxs-lookup"><span data-stu-id="d2e73-130">System.String</span></span>

### <span data-ttu-id="d2e73-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d2e73-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="d2e73-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d2e73-132">OUTPUTS</span></span>

### <span data-ttu-id="d2e73-133">System. void</span><span class="sxs-lookup"><span data-stu-id="d2e73-133">System.Void</span></span>

## <span data-ttu-id="d2e73-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="d2e73-134">NOTES</span></span>

## <span data-ttu-id="d2e73-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d2e73-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2e73-136">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e73-136">Get-AzureRmBatchApplication</span></span>](./Get-AzureRmBatchApplication.md)

[<span data-ttu-id="d2e73-137">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e73-137">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2e73-138">Neu – AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e73-138">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="d2e73-139">Neu – AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e73-139">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="d2e73-140">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="d2e73-140">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="d2e73-141">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="d2e73-141">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)


