---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FF111B74-90A3-4F7C-B515-CE1EEF68EB54
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/new-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/New-AzBatchApplication.md
ms.openlocfilehash: 0c1d847045cc4fb8be39674c13c38114ee9d3a57
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93661669"
---
# <span data-ttu-id="74f34-101">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74f34-101">New-AzBatchApplication</span></span>

## <span data-ttu-id="74f34-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="74f34-102">SYNOPSIS</span></span>
<span data-ttu-id="74f34-103">Fügt dem angegebenen Batch Konto eine Anwendung hinzu.</span><span class="sxs-lookup"><span data-stu-id="74f34-103">Adds an application to the specified Batch account.</span></span>

## <span data-ttu-id="74f34-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="74f34-104">SYNTAX</span></span>

```
New-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationId] <String>
 [[-AllowUpdates] <Boolean>] [[-DisplayName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="74f34-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="74f34-105">DESCRIPTION</span></span>
<span data-ttu-id="74f34-106">Mit dem Cmdlet **New-AzBatchApplication** wird eine Anwendung zum angegebenen Azure-Batch Konto hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="74f34-106">The **New-AzBatchApplication** cmdlet adds an application to the specified Azure Batch account.</span></span>

## <span data-ttu-id="74f34-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="74f34-107">EXAMPLES</span></span>

### <span data-ttu-id="74f34-108">Beispiel 1: Hinzufügen einer leeren Anwendung zu einem Stapelverarbeitungs Konto</span><span class="sxs-lookup"><span data-stu-id="74f34-108">Example 1: Add an empty application to a Batch account</span></span>
```
PS C:\>New-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "Litware" -AllowUpdates $True -DisplayName "Litware Advanced Reticulator"
```

<span data-ttu-id="74f34-109">Mit diesem Befehl wird die Litware-Anwendung im ContosoBatch-Konto erstellt.</span><span class="sxs-lookup"><span data-stu-id="74f34-109">This command creates the Litware application in the ContosoBatch account.</span></span>
<span data-ttu-id="74f34-110">Die Anwendung enthält zunächst keine Pakete.</span><span class="sxs-lookup"><span data-stu-id="74f34-110">The application initially contains no packages.</span></span>

## <span data-ttu-id="74f34-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="74f34-111">PARAMETERS</span></span>

### <span data-ttu-id="74f34-112">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="74f34-112">-AccountName</span></span>
<span data-ttu-id="74f34-113">Gibt den Namen des Batch Kontos an, dem dieses Cmdlet eine Anwendung hinzufügt.</span><span class="sxs-lookup"><span data-stu-id="74f34-113">Specifies the name of the Batch account to which this cmdlet adds an application.</span></span>

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

### <span data-ttu-id="74f34-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="74f34-114">-AllowUpdates</span></span>
<span data-ttu-id="74f34-115">Gibt an, ob Pakete in der Anwendung mit der gleichen Versionszeichenfolge überschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="74f34-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

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

### <span data-ttu-id="74f34-116">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="74f34-116">-ApplicationId</span></span>
<span data-ttu-id="74f34-117">Gibt die ID der Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="74f34-117">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="74f34-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74f34-118">-DefaultProfile</span></span>
<span data-ttu-id="74f34-119">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="74f34-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="74f34-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="74f34-120">-DisplayName</span></span>
<span data-ttu-id="74f34-121">Gibt den Anzeigenamen für die Anwendung an.</span><span class="sxs-lookup"><span data-stu-id="74f34-121">Specifies the display name for the application.</span></span>

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

### <span data-ttu-id="74f34-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74f34-122">-ResourceGroupName</span></span>
<span data-ttu-id="74f34-123">Gibt den Namen der Ressourcengruppe an, die das Stapelverarbeitungs Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="74f34-123">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="74f34-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74f34-124">CommonParameters</span></span>
<span data-ttu-id="74f34-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="74f34-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74f34-126">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="74f34-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74f34-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="74f34-127">INPUTS</span></span>

### <span data-ttu-id="74f34-128">System. String</span><span class="sxs-lookup"><span data-stu-id="74f34-128">System.String</span></span>

### <span data-ttu-id="74f34-129">System. Nullable ' 1 [[System. Boolean, System. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="74f34-129">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="74f34-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="74f34-130">OUTPUTS</span></span>

### <span data-ttu-id="74f34-131">Microsoft.Azure.Commands.Batch. Models. PSApplication</span><span class="sxs-lookup"><span data-stu-id="74f34-131">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="74f34-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="74f34-132">NOTES</span></span>

## <span data-ttu-id="74f34-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="74f34-133">RELATED LINKS</span></span>

[<span data-ttu-id="74f34-134">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74f34-134">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="74f34-135">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74f34-135">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="74f34-136">Neu – AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74f34-136">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="74f34-137">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74f34-137">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="74f34-138">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="74f34-138">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="74f34-139">Satz-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="74f34-139">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


