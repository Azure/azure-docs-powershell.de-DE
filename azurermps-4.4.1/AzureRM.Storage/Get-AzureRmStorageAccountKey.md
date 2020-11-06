---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccountKey.md
ms.openlocfilehash: d12be29507f581f3e9a8d0de86d8a571a305908d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93483257"
---
# <span data-ttu-id="7eeeb-101">Get-AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7eeeb-101">Get-AzureRmStorageAccountKey</span></span>

## <span data-ttu-id="7eeeb-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="7eeeb-102">SYNOPSIS</span></span>
<span data-ttu-id="7eeeb-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-103">Gets the access keys for an Azure Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7eeeb-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="7eeeb-104">SYNTAX</span></span>

```
Get-AzureRmStorageAccountKey [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7eeeb-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7eeeb-105">DESCRIPTION</span></span>
<span data-ttu-id="7eeeb-106">Das Cmdlet " **Get-AzureRmStorageAccountKey** " Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-106">The **Get-AzureRmStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="7eeeb-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="7eeeb-107">EXAMPLES</span></span>

### <span data-ttu-id="7eeeb-108">Beispiel 1: Abrufen der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7eeeb-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="7eeeb-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="7eeeb-110">Beispiel 2: Abrufen einer bestimmten Zugriffstaste für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="7eeeb-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Value[0]

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzureRmStorageAccountKey -ResourceGroupName "RG01" -AccountName "MyStorageAccount").Key1
```

## <span data-ttu-id="7eeeb-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="7eeeb-111">PARAMETERS</span></span>

### <span data-ttu-id="7eeeb-112">-Name</span><span class="sxs-lookup"><span data-stu-id="7eeeb-112">-Name</span></span>
<span data-ttu-id="7eeeb-113">Gibt den Namen des speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-113">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7eeeb-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7eeeb-114">-ResourceGroupName</span></span>
<span data-ttu-id="7eeeb-115">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-115">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="7eeeb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7eeeb-116">-DefaultProfile</span></span>
<span data-ttu-id="7eeeb-117">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7eeeb-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7eeeb-118">CommonParameters</span></span>
<span data-ttu-id="7eeeb-119">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7eeeb-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7eeeb-120">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7eeeb-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7eeeb-121">Eingaben</span><span class="sxs-lookup"><span data-stu-id="7eeeb-121">INPUTS</span></span>

## <span data-ttu-id="7eeeb-122">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="7eeeb-122">OUTPUTS</span></span>

## <span data-ttu-id="7eeeb-123">Notizen</span><span class="sxs-lookup"><span data-stu-id="7eeeb-123">NOTES</span></span>

## <span data-ttu-id="7eeeb-124">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="7eeeb-124">RELATED LINKS</span></span>

[<span data-ttu-id="7eeeb-125">Neu – AzureRmStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="7eeeb-125">New-AzureRmStorageAccountKey</span></span>](./New-AzureRmStorageAccountKey.md)


