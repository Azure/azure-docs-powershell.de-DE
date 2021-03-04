---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: BF5526C1-11B9-47A8-A5A6-CB275B470A9E
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstoragetablestoredaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageTableStoredAccessPolicy.md
ms.openlocfilehash: 2de23408aef9d9af4ebd23eb520261760883cf3a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 03/04/2021
ms.locfileid: "101940752"
---
# <span data-ttu-id="f19a1-101">Get-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f19a1-101">Get-AzStorageTableStoredAccessPolicy</span></span>

## <span data-ttu-id="f19a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f19a1-102">SYNOPSIS</span></span>
<span data-ttu-id="f19a1-103">Ruft die Richtlinie für den gespeicherten Zugriff oder die Richtlinien für eine Azure-Speichertabelle ab.</span><span class="sxs-lookup"><span data-stu-id="f19a1-103">Gets the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="f19a1-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="f19a1-104">SYNTAX</span></span>

```
Get-AzStorageTableStoredAccessPolicy [-Table] <String> [[-Policy] <String>] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f19a1-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="f19a1-105">DESCRIPTION</span></span>
<span data-ttu-id="f19a1-106">Im **Cmdlet Get-AzStorageTableStoredAccessPolicy** werden die Gespeicherten Zugriffsrichtlinien oder Richtlinien für eine Azure-Speichertabelle aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f19a1-106">The **Get-AzStorageTableStoredAccessPolicy** cmdlet lists the stored access policy or policies for an Azure storage table.</span></span>

## <span data-ttu-id="f19a1-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="f19a1-107">EXAMPLES</span></span>

### <span data-ttu-id="f19a1-108">Beispiel 1: Erhalten einer gespeicherten Zugriffsrichtlinie in einer Speichertabelle</span><span class="sxs-lookup"><span data-stu-id="f19a1-108">Example 1: Get a stored access policy in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02" -Policy "Policy50"
```

<span data-ttu-id="f19a1-109">Dieser Befehl ruft die Zugriffsrichtlinie mit dem Namen Policy50 in der Speichertabelle mit dem Namen Table02 ab.</span><span class="sxs-lookup"><span data-stu-id="f19a1-109">This command gets the access policy named Policy50 in the storage table named Table02.</span></span>

### <span data-ttu-id="f19a1-110">Beispiel 2: Alle Richtlinien für den gespeicherten Zugriff in einer Speichertabelle erhalten</span><span class="sxs-lookup"><span data-stu-id="f19a1-110">Example 2: Get all stored access policies in a storage table</span></span>
```
PS C:\>Get-AzStorageTableStoredAccessPolicy -Table "Table02"
```

<span data-ttu-id="f19a1-111">Dieser Befehl ruft alle Zugriffsrichtlinien in der Tabelle mit dem Namen "Tabelle02" ab.</span><span class="sxs-lookup"><span data-stu-id="f19a1-111">This command gets all access policies in the table named Table02.</span></span>

## <span data-ttu-id="f19a1-112">PARAMETER</span><span class="sxs-lookup"><span data-stu-id="f19a1-112">PARAMETERS</span></span>

### <span data-ttu-id="f19a1-113">-Context</span><span class="sxs-lookup"><span data-stu-id="f19a1-113">-Context</span></span>
<span data-ttu-id="f19a1-114">Gibt den Azure-Speicherkontext an.</span><span class="sxs-lookup"><span data-stu-id="f19a1-114">Specifies the Azure storage context.</span></span>
<span data-ttu-id="f19a1-115">Verwenden Sie zum Abrufen eines Speicherkontexts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f19a1-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f19a1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f19a1-116">-DefaultProfile</span></span>
<span data-ttu-id="f19a1-117">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f19a1-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f19a1-118">-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="f19a1-118">-Policy</span></span>
<span data-ttu-id="f19a1-119">Gibt eine Richtlinie für den gespeicherten Zugriff an, die die Berechtigungen für dieses SAS-Token (Shared Access Signature) enthält.</span><span class="sxs-lookup"><span data-stu-id="f19a1-119">Specifies a stored access policy, which includes the permissions for this Shared Access Signature (SAS) token.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f19a1-120">-Table</span><span class="sxs-lookup"><span data-stu-id="f19a1-120">-Table</span></span>
<span data-ttu-id="f19a1-121">Gibt den Namen der Azure-Speichertabelle an.</span><span class="sxs-lookup"><span data-stu-id="f19a1-121">Specifies the Azure storage table name.</span></span>

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

### <span data-ttu-id="f19a1-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f19a1-122">CommonParameters</span></span>
<span data-ttu-id="f19a1-123">Dieses Cmdlet unterstützt die gängigen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f19a1-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f19a1-124">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f19a1-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f19a1-125">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="f19a1-125">INPUTS</span></span>

### <span data-ttu-id="f19a1-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f19a1-126">System.String</span></span>

### <span data-ttu-id="f19a1-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f19a1-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f19a1-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="f19a1-128">OUTPUTS</span></span>

### <span data-ttu-id="f19a1-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span><span class="sxs-lookup"><span data-stu-id="f19a1-129">Microsoft.WindowsAzure.Storage.Table.SharedAccessTablePolicy</span></span>

## <span data-ttu-id="f19a1-130">NOTIZEN</span><span class="sxs-lookup"><span data-stu-id="f19a1-130">NOTES</span></span>

## <span data-ttu-id="f19a1-131">VERWANDTE LINKS</span><span class="sxs-lookup"><span data-stu-id="f19a1-131">RELATED LINKS</span></span>

[<span data-ttu-id="f19a1-132">New-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f19a1-132">New-AzStorageTableStoredAccessPolicy</span></span>](./New-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f19a1-133">Remove-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f19a1-133">Remove-AzStorageTableStoredAccessPolicy</span></span>](./Remove-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f19a1-134">Set-AzStorageTableStoredAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="f19a1-134">Set-AzStorageTableStoredAccessPolicy</span></span>](./Set-AzStorageTableStoredAccessPolicy.md)

[<span data-ttu-id="f19a1-135">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="f19a1-135">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


