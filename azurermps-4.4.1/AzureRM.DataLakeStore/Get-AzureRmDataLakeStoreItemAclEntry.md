---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: DFE8C373-2BBA-4A4E-B4B1-926373E68FC4
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Get-AzureRmDataLakeStoreItemAclEntry.md
ms.openlocfilehash: 2532b8fb63fb864cf2c70b9e2bfd1d5ef1a5365e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663959"
---
# <span data-ttu-id="c7cea-101">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7cea-101">Get-AzureRmDataLakeStoreItemAclEntry</span></span>

## <span data-ttu-id="c7cea-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="c7cea-102">SYNOPSIS</span></span>
<span data-ttu-id="c7cea-103">Ruft einen Eintrag in der ACL einer Datei oder eines Ordners im Data Lake Store ab.</span><span class="sxs-lookup"><span data-stu-id="c7cea-103">Gets an entry in the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c7cea-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="c7cea-104">SYNTAX</span></span>

```
Get-AzureRmDataLakeStoreItemAclEntry [-Account] <String> [-Path] <DataLakeStorePathInstance>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c7cea-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c7cea-105">DESCRIPTION</span></span>
<span data-ttu-id="c7cea-106">Das Cmdlet " **Get-AzureRmDataLakeStoreItemAclEntry** " ruft in der Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store einen Eintrag (ACE) ab.</span><span class="sxs-lookup"><span data-stu-id="c7cea-106">The **Get-AzureRmDataLakeStoreItemAclEntry** cmdlet gets an entry (ACE) in the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="c7cea-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="c7cea-107">EXAMPLES</span></span>

### <span data-ttu-id="c7cea-108">Beispiel 1: Abrufen der ACL für einen Ordner</span><span class="sxs-lookup"><span data-stu-id="c7cea-108">Example 1: Get the ACL for a folder</span></span>
```
PS C:\> Get-AzureRmDataLakeStoreItemAclEntry -AccountName 'ContosoADL' -Path '/'
```

<span data-ttu-id="c7cea-109">Mit diesem Befehl wird die ACL für das Stammverzeichnis des angegebenen Data Lake Store-Kontos abgerufen.</span><span class="sxs-lookup"><span data-stu-id="c7cea-109">This command gets the ACL for the root directory of the specified Data Lake Store account</span></span>

## <span data-ttu-id="c7cea-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="c7cea-110">PARAMETERS</span></span>

### <span data-ttu-id="c7cea-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="c7cea-111">-Account</span></span>
<span data-ttu-id="c7cea-112">Gibt den Namen des Data Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="c7cea-112">Specifies the name of the Data Lake Store account.</span></span>

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

### <span data-ttu-id="c7cea-113">-Path</span><span class="sxs-lookup"><span data-stu-id="c7cea-113">-Path</span></span>
<span data-ttu-id="c7cea-114">Gibt den Daten See-Speicherpfad des Elements an, für das dieses Cmdlet ab dem Stammverzeichnis (/) ein Ass erhält.</span><span class="sxs-lookup"><span data-stu-id="c7cea-114">Specifies the Data Lake Store path of the item for which this cmdlet gets an ACE, starting with the root directory (/).</span></span>

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

### <span data-ttu-id="c7cea-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c7cea-115">-DefaultProfile</span></span>
<span data-ttu-id="c7cea-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="c7cea-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c7cea-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c7cea-117">CommonParameters</span></span>
<span data-ttu-id="c7cea-118">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c7cea-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c7cea-119">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c7cea-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c7cea-120">Eingaben</span><span class="sxs-lookup"><span data-stu-id="c7cea-120">INPUTS</span></span>

## <span data-ttu-id="c7cea-121">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="c7cea-121">OUTPUTS</span></span>

### <span data-ttu-id="c7cea-122">IEnumerable<DataLakeStoreItemAce></span><span class="sxs-lookup"><span data-stu-id="c7cea-122">IEnumerable<DataLakeStoreItemAce></span></span>
<span data-ttu-id="c7cea-123">Die Liste der ACL-Einträge für den angegebenen Ordner oder die angegebene Datei.</span><span class="sxs-lookup"><span data-stu-id="c7cea-123">The list of ACL entries for the specified folder or file.</span></span>

## <span data-ttu-id="c7cea-124">Notizen</span><span class="sxs-lookup"><span data-stu-id="c7cea-124">NOTES</span></span>

## <span data-ttu-id="c7cea-125">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="c7cea-125">RELATED LINKS</span></span>

[<span data-ttu-id="c7cea-126">Remove-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7cea-126">Remove-AzureRmDataLakeStoreItemAclEntry</span></span>](./Remove-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="c7cea-127">Satz-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="c7cea-127">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


