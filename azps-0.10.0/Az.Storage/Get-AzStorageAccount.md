---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: E53D5040-C1E8-4DC1-8371-F41C00B666E3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageAccount.md
ms.openlocfilehash: be32e761fc854c6ad4a270f36e4c9b6328e00ba1
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93843127"
---
# <span data-ttu-id="66dee-101">Get-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66dee-101">Get-AzStorageAccount</span></span>

## <span data-ttu-id="66dee-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="66dee-102">SYNOPSIS</span></span>
<span data-ttu-id="66dee-103">Ruft ein Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="66dee-103">Gets a Storage account.</span></span>

## <span data-ttu-id="66dee-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="66dee-104">SYNTAX</span></span>

### <span data-ttu-id="66dee-105">ResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="66dee-105">ResourceGroupParameterSet</span></span>
```
Get-AzStorageAccount [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="66dee-106">AccountNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66dee-106">AccountNameParameterSet</span></span>
```
Get-AzStorageAccount [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="66dee-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="66dee-107">DESCRIPTION</span></span>
<span data-ttu-id="66dee-108">Das Cmdlet " **Get-AzStorageAccount** " Ruft ein bestimmtes Speicherkonto oder alle Speicherkonten in einer Ressourcengruppe oder dem Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="66dee-108">The **Get-AzStorageAccount** cmdlet gets a specified Storage account or all of the Storage accounts in a resource group or the subscription.</span></span>

## <span data-ttu-id="66dee-109">Beispiele</span><span class="sxs-lookup"><span data-stu-id="66dee-109">EXAMPLES</span></span>

### <span data-ttu-id="66dee-110">Beispiel 1: Abrufen eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="66dee-110">Example 1: Get a specified Storage account</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="66dee-111">Dieser Befehl ruft das angegebene Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="66dee-111">This command gets the specified Storage account.</span></span>

### <span data-ttu-id="66dee-112">Beispiel 2: Abrufen aller Speicherkonten in einer Ressourcengruppe</span><span class="sxs-lookup"><span data-stu-id="66dee-112">Example 2: Get all Storage accounts in a resource group</span></span>
```
PS C:\>Get-AzStorageAccount -ResourceGroupName "RG01"
```

<span data-ttu-id="66dee-113">Dieser Befehl ruft alle Speicherkonten in einer Ressourcengruppe ab.</span><span class="sxs-lookup"><span data-stu-id="66dee-113">This command gets all of the Storage accounts in a resource group.</span></span>

### <span data-ttu-id="66dee-114">Beispiel 3: Abrufen aller Speicherkonten im Abonnement</span><span class="sxs-lookup"><span data-stu-id="66dee-114">Example 3:  Get all Storage accounts in the subscription</span></span>
```
PS C:\>Get-AzStorageAccount
```

<span data-ttu-id="66dee-115">Dieser Befehl ruft alle Speicherkonten des Abonnements ab.</span><span class="sxs-lookup"><span data-stu-id="66dee-115">This command gets all of the Storage accounts in the subscription.</span></span>

## <span data-ttu-id="66dee-116">Parameter</span><span class="sxs-lookup"><span data-stu-id="66dee-116">PARAMETERS</span></span>

### <span data-ttu-id="66dee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66dee-117">-DefaultProfile</span></span>
<span data-ttu-id="66dee-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="66dee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66dee-119">-Name</span><span class="sxs-lookup"><span data-stu-id="66dee-119">-Name</span></span>
<span data-ttu-id="66dee-120">Gibt den Namen des abzurufenden speicherkontos an.</span><span class="sxs-lookup"><span data-stu-id="66dee-120">Specifies the name of the Storage account to get.</span></span>

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

### <span data-ttu-id="66dee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="66dee-121">-ResourceGroupName</span></span>
<span data-ttu-id="66dee-122">Gibt den Namen der Ressourcengruppe an, die das abzurufende Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="66dee-122">Specifies the name of the resource group that contains the Storage account to get.</span></span>

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

### <span data-ttu-id="66dee-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66dee-123">CommonParameters</span></span>
<span data-ttu-id="66dee-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="66dee-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66dee-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="66dee-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66dee-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="66dee-126">INPUTS</span></span>

### <span data-ttu-id="66dee-127">System. String</span><span class="sxs-lookup"><span data-stu-id="66dee-127">System.String</span></span>

## <span data-ttu-id="66dee-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="66dee-128">OUTPUTS</span></span>

### <span data-ttu-id="66dee-129">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66dee-129">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

## <span data-ttu-id="66dee-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="66dee-130">NOTES</span></span>

## <span data-ttu-id="66dee-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="66dee-131">RELATED LINKS</span></span>

[<span data-ttu-id="66dee-132">Neu – AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66dee-132">New-AzStorageAccount</span></span>](./New-AzStorageAccount.md)

[<span data-ttu-id="66dee-133">Remove-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66dee-133">Remove-AzStorageAccount</span></span>](./Remove-AzStorageAccount.md)

[<span data-ttu-id="66dee-134">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="66dee-134">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


