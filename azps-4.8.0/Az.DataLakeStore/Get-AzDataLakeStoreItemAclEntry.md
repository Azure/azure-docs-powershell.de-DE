---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/get-azdatalakestoreitemaclentry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Get-AzDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 02ff6856cf61664c1bd00e7d88fc7f8de999f2a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94174781"
---
# <span data-ttu-id="fb69c-101">Get-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fb69c-101">Get-AzDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="fb69c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fb69c-102">SYNOPSIS</span></span>
<span data-ttu-id="fb69c-103">Ruft einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="fb69c-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fb69c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fb69c-104">SYNTAX</span></span>

```
Get-AzDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb69c-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fb69c-105">DESCRIPTION</span></span>
<span data-ttu-id="fb69c-106">Das Cmdlet " **Get-AzDataLakeStoreItemAclEntry** " ruft in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store einen Eintrag (ACE) ab.</span><span class="sxs-lookup"><span data-stu-id="fb69c-106">The **Get-AzDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="fb69c-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fb69c-107">EXAMPLES</span></span>

### <span data-ttu-id="fb69c-108">Beispiel 1: Abrufen der ACL für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="fb69c-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="fb69c-109">Mit diesem Befehl wird die ACL für das Stammverzeichnis des angegebenen Data Lake Store-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="fb69c-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="fb69c-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="fb69c-110">PARAMETERS</span></span>

### <span data-ttu-id="fb69c-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="fb69c-111">-Account</span></span>
<span data-ttu-id="fb69c-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="fb69c-112">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb69c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb69c-113">-DefaultProfile</span></span>
<span data-ttu-id="fb69c-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fb69c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb69c-115">-Path</span><span class="sxs-lookup"><span data-stu-id="fb69c-115">-Path</span></span>
<span data-ttu-id="fb69c-116">Gibt den Daten See-Speicherpfad des Elements an, für das dieses Cmdlet ab dem Stammverzeichnis (/) ein Ass erhält.</span><span class="sxs-lookup"><span data-stu-id="fb69c-116">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fb69c-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb69c-117">CommonParameters</span></span>
<span data-ttu-id="fb69c-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb69c-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb69c-119">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb69c-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb69c-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fb69c-120">INPUTS</span></span>

### <span data-ttu-id="fb69c-121">System. String</span><span class="sxs-lookup"><span data-stu-id="fb69c-121">System.String</span></span>

### <span data-ttu-id="fb69c-122">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStorePathInstance</span><span class="sxs-lookup"><span data-stu-id="fb69c-122">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStorePathInstance</span></span>

## <span data-ttu-id="fb69c-123">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fb69c-123">OUTPUTS</span></span>

### <span data-ttu-id="fb69c-124">Microsoft. Azure. Commands. DataLakeStore. Models. DataLakeStoreItemAce</span><span class="sxs-lookup"><span data-stu-id="fb69c-124">Microsoft.Azure.Commands.DataLakeStore.Models.DataLakeStoreItemAce</span></span>

## <span data-ttu-id="fb69c-125">Notizen</span><span class="sxs-lookup"><span data-stu-id="fb69c-125">NOTES</span></span>

## <span data-ttu-id="fb69c-126">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fb69c-126">RELATED LINKS</span></span>

[<span data-ttu-id="fb69c-127">Remove-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fb69c-127">Remove-AzDataLakeStoreItemAclEntry</span></span>](./Remove-AzDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="fb69c-128">Satz-AzDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="fb69c-128">Set-AzDataLakeStoreItemAclEntry</span></span>](./Set-AzDataLakeStoreItemAclEntry.md)


