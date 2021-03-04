---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: cf783e708f4e37de209681e65d19f51ea6aea80b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101924376"
---
# <span data-ttu-id="1b5b9-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b5b9-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="1b5b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b5b9-102">SYNOPSIS</span></span>
<span data-ttu-id="1b5b9-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="1b5b9-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="1b5b9-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b5b9-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="1b5b9-105">DESCRIPTION</span></span>
<span data-ttu-id="1b5b9-106">Das **Cmdlet New-AzStorageTableStoredAccessPolicy** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="1b5b9-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="1b5b9-107">EXAMPLES</span></span>

### <span data-ttu-id="1b5b9-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="1b5b9-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="1b5b9-109">Mit diesem Befehl wird in der Speichertabelle "MyTable" eine Zugriffsrichtlinie mit dem Namen "Policy02" erstellt.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="1b5b9-110">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="1b5b9-110">PARAMETERS</span></span>

### <span data-ttu-id="1b5b9-111">-Context</span><span class="sxs-lookup"><span data-stu-id="1b5b9-111">-Context</span></span>
<span data-ttu-id="1b5b9-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1b5b9-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b5b9-114">-DefaultProfile</span></span>
<span data-ttu-id="1b5b9-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="1b5b9-116">-ExpiryTime</span></span>
<span data-ttu-id="1b5b9-117">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="1b5b9-118">-Permission</span></span>
<span data-ttu-id="1b5b9-119">Gibt Berechtigungen in der Richtlinie für den gespeicherten Zugriff für den Zugriff auf die Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="1b5b9-120">Beachten Sie, dass es sich um eine Zeichenfolge handelt, z. B. `raud` (für Lesen, Hinzufügen, Aktualisieren und Löschen).</span><span class="sxs-lookup"><span data-stu-id="1b5b9-120">It is important to note that this is a string, like `raud` (for Read, Add, Update and Delete).</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-121">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="1b5b9-121">-Policy</span></span>
<span data-ttu-id="1b5b9-122">Gibt einen Namen für die gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="1b5b9-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1b5b9-123">-StartTime</span></span>
<span data-ttu-id="1b5b9-124">Gibt den Zeitpunkt an, zu dem die gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-124">Specifies the time at which the stored access policy becomes valid.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-125">-Table</span><span class="sxs-lookup"><span data-stu-id="1b5b9-125">-Table</span></span>
<span data-ttu-id="1b5b9-126">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-126">Specifies the Azure storage table name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: N, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b5b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b5b9-127">CommonParameters</span></span>
<span data-ttu-id="1b5b9-128">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b5b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b5b9-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b5b9-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b5b9-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="1b5b9-130">INPUTS</span></span>

### <span data-ttu-id="1b5b9-131">System.String</span><span class="sxs-lookup"><span data-stu-id="1b5b9-131">System.String</span></span>

### <span data-ttu-id="1b5b9-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b5b9-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1b5b9-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="1b5b9-133">OUTPUTS</span></span>

### <span data-ttu-id="1b5b9-134">System.String</span><span class="sxs-lookup"><span data-stu-id="1b5b9-134">System.String</span></span>

## <span data-ttu-id="1b5b9-135">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="1b5b9-135">NOTES</span></span>

## <span data-ttu-id="1b5b9-136">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="1b5b9-136">RELATED LINKS</span></span>

[<span data-ttu-id="1b5b9-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b5b9-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1b5b9-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b5b9-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="1b5b9-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b5b9-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="1b5b9-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="1b5b9-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


