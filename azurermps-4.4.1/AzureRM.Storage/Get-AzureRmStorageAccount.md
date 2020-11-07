---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Stack/Commands.Management.Storage/help/Get-AzureRmStorageAccount.md
ms.openlocfilehash: 07fdf5a05f5099facabb78f35c44856545d1efe3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93662766"
---
# <span data-ttu-id="fa037-101">Get-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa037-101">Get-AzureRmStorageAccount</span></span>

## <span data-ttu-id="fa037-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="fa037-102">SYNOPSIS</span></span>
<span data-ttu-id="fa037-103">Ruft ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="fa037-103">Gets a Storage account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fa037-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="fa037-104">SYNTAX</span></span>

### <span data-ttu-id="fa037-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa037-105">ResourceGroupParameterSet</span></span>
```
Get-AzureRmStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="fa037-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="fa037-106">AccountNameParameterSet</span></span>
```
Get-AzureRmStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fa037-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fa037-107">DESCRIPTION</span></span>
<span data-ttu-id="fa037-108">Das Cmdlet " **Get-AzureRmStorageAccount** " Ruft ein bestimmtes Speicherkonto oder alle Speicherkonten in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="fa037-108">The **Get-AzureRmStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="fa037-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="fa037-109">EXAMPLES</span></span>

### <span data-ttu-id="fa037-110">Beispiel 1: Abrufen eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="fa037-110">Example 1: Get a specified storage account</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01" -AccountName "MyStorageAccount"
```

<span data-ttu-id="fa037-111">Dieser Befehl ruft das angegebene Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="fa037-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="fa037-112">Beispiel 2: Abrufen aller Speicherkonten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="fa037-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzureRmStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="fa037-113">Dieser Befehl ruft alle Speicherkonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="fa037-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="fa037-114">Beispiel 3: Abrufen aller Speicherkonten im Abonnement</span><span class="sxs-lookup"><span data-stu-id="fa037-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzureRmStorageAccount
```

<span data-ttu-id="fa037-115">Dieser Befehl ruft alle Speicherkonten des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="fa037-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="fa037-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="fa037-116">PARAMETERS</span></span>

### <span data-ttu-id="fa037-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fa037-117">-Name</span></span>
<span data-ttu-id="fa037-118">Gibt den Namen des abzurufenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="fa037-118">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="fa037-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fa037-119">-ResourceGroupName</span></span>
<span data-ttu-id="fa037-120">Gibt den Namen der Ressourcengruppe an, die das abzurufende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="fa037-120">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="fa037-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fa037-121">-DefaultProfile</span></span>
<span data-ttu-id="fa037-122">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="fa037-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fa037-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fa037-123">CommonParameters</span></span>
<span data-ttu-id="fa037-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fa037-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fa037-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fa037-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fa037-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="fa037-126">INPUTS</span></span>

## <span data-ttu-id="fa037-127">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="fa037-127">OUTPUTS</span></span>

## <span data-ttu-id="fa037-128">Notizen</span><span class="sxs-lookup"><span data-stu-id="fa037-128">NOTES</span></span>

## <span data-ttu-id="fa037-129">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="fa037-129">RELATED LINKS</span></span>

[<span data-ttu-id="fa037-130">Neu – AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa037-130">New-AzureRmStorageAccount</span></span>](./New-AzureRmStorageAccount.md)

[<span data-ttu-id="fa037-131">Remove-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa037-131">Remove-AzureRmStorageAccount</span></span>](./Remove-AzureRmStorageAccount.md)

[<span data-ttu-id="fa037-132">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="fa037-132">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


