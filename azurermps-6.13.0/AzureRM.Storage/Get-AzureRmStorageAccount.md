---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: bf63046ebe8b73f97a80e1465060b6265f99923e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662294"
---
# <span data-ttu-id="3715c-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3715c-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="3715c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3715c-102">SYNOPSIS</span></span>
<span data-ttu-id="3715c-103">Ruft ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="3715c-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3715c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3715c-104">SYNTAX</span></span>

### <span data-ttu-id="3715c-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="3715c-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="3715c-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3715c-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3715c-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3715c-107">DESCRIPTION</span></span>
<span data-ttu-id="3715c-108">Das Cmdlet " **Get-AzureRmStorageAccount** " Ruft ein bestimmtes Speicherkonto oder alle Speicherkonten in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="3715c-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="3715c-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3715c-109">EXAMPLES</span></span>

### <span data-ttu-id="3715c-110">Beispiel 1: Abrufen eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="3715c-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="3715c-111">Dieser Befehl ruft das angegebene Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="3715c-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="3715c-112">Beispiel 2: Abrufen aller Speicherkonten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="3715c-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="3715c-113">Dieser Befehl ruft alle Speicherkonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="3715c-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="3715c-114">Beispiel 3: Abrufen aller Speicherkonten im Abonnement</span><span class="sxs-lookup"><span data-stu-id="3715c-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="3715c-115">Dieser Befehl ruft alle Speicherkonten des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="3715c-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="3715c-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="3715c-116">PARAMETERS</span></span>

### <span data-ttu-id="3715c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3715c-117">-DefaultProfile</span></span>
<span data-ttu-id="3715c-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="3715c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3715c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3715c-119">-Name</span></span>
<span data-ttu-id="3715c-120">Gibt den Namen des abzurufenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="3715c-120">Specifies the name of the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3715c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3715c-121">-ResourceGroupName</span></span>
<span data-ttu-id="3715c-122">Gibt den Namen der Ressourcengruppe an, die das abzurufende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="3715c-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: AccountNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3715c-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3715c-123">CommonParameters</span></span>
<span data-ttu-id="3715c-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3715c-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3715c-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3715c-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3715c-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3715c-126">INPUTS</span></span>

### <span data-ttu-id="3715c-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3715c-127">System.String</span></span>

## <span data-ttu-id="3715c-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3715c-128">OUTPUTS</span></span>

### <span data-ttu-id="3715c-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3715c-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="3715c-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="3715c-130">NOTES</span></span>

## <span data-ttu-id="3715c-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3715c-131">RELATED LINKS</span></span>

[<span data-ttu-id="3715c-132">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3715c-132">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="3715c-133">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3715c-133">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="3715c-134">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="3715c-134">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


