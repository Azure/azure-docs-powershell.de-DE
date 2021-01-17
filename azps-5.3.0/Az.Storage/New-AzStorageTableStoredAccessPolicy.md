---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: CF3B6E3B-3FC1-4871-AFE0-366B17A9E4F8
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/new-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/New-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 82e5d252e2e8185b98c142b24537c666e5618d7f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98471706"
---
# <span data-ttu-id="62546-101">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62546-101">New-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="62546-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62546-102">SYNOPSIS</span></span>
<span data-ttu-id="62546-103">Erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="62546-103">Creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="62546-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="62546-104">SYNTAX</span></span>

```
New-AzStorageTableStoredAccessPolicy [-Table] <String> [-Policy] <String> [-Permission <String>]
 [-StartTime <DateTime>] [-ExpiryTime <DateTime>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62546-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="62546-105">DESCRIPTION</span></span>
<span data-ttu-id="62546-106">Das **Cmdlet "New-AzStorageTableStoredAccessPolicy"** erstellt eine gespeicherte Zugriffsrichtlinie für eine Azure-Speichertabelle.</span><span class="sxs-lookup"><span data-stu-id="62546-106">The **New-AzStorageTableStoredAccessPolicy** cmdlet creates a stored access policy for an Azure storage table.</span></span>

## <span data-ttu-id="62546-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="62546-107">EXAMPLES</span></span>

### <span data-ttu-id="62546-108">Beispiel 1: Erstellen einer gespeicherten Zugriffsrichtlinie in einer Tabelle</span><span class="sxs-lookup"><span data-stu-id="62546-108">Example 1: Create a stored access policy in a table</span></span>
```
PS C:\>New-AzStorageTableStoredAccessPolicy -Table "MyTable" -Policy "Policy02"
```

<span data-ttu-id="62546-109">Mit diesem Befehl wird eine Zugriffsrichtlinie mit dem Namen "Policy02" in der Speichertabelle "MyTable" erstellt.</span><span class="sxs-lookup"><span data-stu-id="62546-109">This command creates an access policy named Policy02 in the storage table named MyTable.</span></span>

## <span data-ttu-id="62546-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62546-110">PARAMETERS</span></span>

### <span data-ttu-id="62546-111">-Context</span><span class="sxs-lookup"><span data-stu-id="62546-111">-Context</span></span>
<span data-ttu-id="62546-112">Gibt einen Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="62546-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="62546-113">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62546-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="62546-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62546-114">-DefaultProfile</span></span>
<span data-ttu-id="62546-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="62546-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62546-116">-ExpiryTime</span><span class="sxs-lookup"><span data-stu-id="62546-116">-ExpiryTime</span></span>
<span data-ttu-id="62546-117">Gibt den Zeitpunkt an, zu dem die Richtlinie für den gespeicherten Zugriff ungültig wird.</span><span class="sxs-lookup"><span data-stu-id="62546-117">Specifies the time at which the stored access policy becomes invalid.</span></span>

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

### <span data-ttu-id="62546-118">-Permission</span><span class="sxs-lookup"><span data-stu-id="62546-118">-Permission</span></span>
<span data-ttu-id="62546-119">Gibt Berechtigungen in der Richtlinie für den gespeicherten Zugriff für den Zugriff auf die Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="62546-119">Specifies permissions in the stored access policy to access the storage table.</span></span>
<span data-ttu-id="62546-120">Beachten Sie, dass es sich um eine Zeichenfolge wie `rwd` "Lesen", "Schreiben" und "Löschen" handelt.</span><span class="sxs-lookup"><span data-stu-id="62546-120">It is important to note that this is a string, like `rwd` (for Read, Write and Delete).</span></span>

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

### <span data-ttu-id="62546-121">-Policy</span><span class="sxs-lookup"><span data-stu-id="62546-121">-Policy</span></span>
<span data-ttu-id="62546-122">Gibt einen Namen für die Gespeicherte Zugriffsrichtlinie an.</span><span class="sxs-lookup"><span data-stu-id="62546-122">Specifies a name for the stored access policy.</span></span>

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

### <span data-ttu-id="62546-123">-StartTime</span><span class="sxs-lookup"><span data-stu-id="62546-123">-StartTime</span></span>
<span data-ttu-id="62546-124">Gibt den Zeitpunkt an, zu dem die Gespeicherte Zugriffsrichtlinie gültig wird.</span><span class="sxs-lookup"><span data-stu-id="62546-124">Specifies the time at which the stored access policy becomes valid.</span></span>

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

### <span data-ttu-id="62546-125">-Table</span><span class="sxs-lookup"><span data-stu-id="62546-125">-Table</span></span>
<span data-ttu-id="62546-126">Gibt den Namen der Azure -Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="62546-126">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="62546-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62546-127">CommonParameters</span></span>
<span data-ttu-id="62546-128">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62546-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62546-129">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62546-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62546-130">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="62546-130">INPUTS</span></span>

### <span data-ttu-id="62546-131">System.String</span><span class="sxs-lookup"><span data-stu-id="62546-131">System.String</span></span>

### <span data-ttu-id="62546-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="62546-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="62546-133">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="62546-133">OUTPUTS</span></span>

### <span data-ttu-id="62546-134">System.String</span><span class="sxs-lookup"><span data-stu-id="62546-134">System.String</span></span>

## <span data-ttu-id="62546-135">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="62546-135">NOTES</span></span>

## <span data-ttu-id="62546-136">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="62546-136">RELATED LINKS</span></span>

[<span data-ttu-id="62546-137">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62546-137">Get-AzStorageTableStoredAccessPolicy</span></span>](./Get-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="62546-138">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="62546-138">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="62546-139">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62546-139">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="62546-140">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="62546-140">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)


