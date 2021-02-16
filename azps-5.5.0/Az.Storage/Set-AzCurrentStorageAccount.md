---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: c57f8a7ce6b4f7275e724c777c2e6dfd54a680ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 02/09/2021
ms.locfileid: "100157956"
---
# <span data-ttu-id="bea5b-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bea5b-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="bea5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea5b-102">SYNOPSIS</span></span>
<span data-ttu-id="bea5b-103">Ändert das aktuelle Speicherkonto des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="bea5b-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="bea5b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="bea5b-104">SYNTAX</span></span>

### <span data-ttu-id="bea5b-105">UsingResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="bea5b-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bea5b-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="bea5b-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bea5b-107">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="bea5b-107">DESCRIPTION</span></span>
<span data-ttu-id="bea5b-108">Das **Cmdlet "Set-AzCurrentStorageAccount"** ändert das aktuelle Azure Storage-Konto des angegebenen Azure-Abonnements in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="bea5b-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="bea5b-109">Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf "Speicher" zugreifen, ohne einen Namen für das Speicherkonto anzugeben.</span><span class="sxs-lookup"><span data-stu-id="bea5b-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="bea5b-110">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="bea5b-110">EXAMPLES</span></span>

### <span data-ttu-id="bea5b-111">Beispiel 1: Festlegen des aktuellen Speicherkontos</span><span class="sxs-lookup"><span data-stu-id="bea5b-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="bea5b-112">Mit diesem Befehl wird das Standardspeicherkonto für das angegebene Abonnement festgelegt.</span><span class="sxs-lookup"><span data-stu-id="bea5b-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="bea5b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bea5b-113">PARAMETERS</span></span>

### <span data-ttu-id="bea5b-114">-Context</span><span class="sxs-lookup"><span data-stu-id="bea5b-114">-Context</span></span>
<span data-ttu-id="bea5b-115">Gibt ein **AzureStorageContext-Objekt** für das aktuelle Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="bea5b-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="bea5b-116">Verwenden Sie zum Abrufen eines Speicherkontextobjekts das New-AzStorageContext Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="bea5b-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: UsingStorageContext
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bea5b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea5b-117">-DefaultProfile</span></span>
<span data-ttu-id="bea5b-118">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bea5b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="bea5b-119">-Name</span><span class="sxs-lookup"><span data-stu-id="bea5b-119">-Name</span></span>
<span data-ttu-id="bea5b-120">Gibt den Namen des Speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="bea5b-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea5b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bea5b-121">-ResourceGroupName</span></span>
<span data-ttu-id="bea5b-122">Gibt die Ressourcengruppe an, die das zu ändernde Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="bea5b-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bea5b-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea5b-123">CommonParameters</span></span>
<span data-ttu-id="bea5b-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bea5b-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea5b-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea5b-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea5b-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="bea5b-126">INPUTS</span></span>

### <span data-ttu-id="bea5b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="bea5b-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="bea5b-128">System.String</span><span class="sxs-lookup"><span data-stu-id="bea5b-128">System.String</span></span>

## <span data-ttu-id="bea5b-129">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="bea5b-129">OUTPUTS</span></span>

### <span data-ttu-id="bea5b-130">System.String</span><span class="sxs-lookup"><span data-stu-id="bea5b-130">System.String</span></span>

## <span data-ttu-id="bea5b-131">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="bea5b-131">NOTES</span></span>

## <span data-ttu-id="bea5b-132">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="bea5b-132">RELATED LINKS</span></span>

[<span data-ttu-id="bea5b-133">Set-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="bea5b-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


