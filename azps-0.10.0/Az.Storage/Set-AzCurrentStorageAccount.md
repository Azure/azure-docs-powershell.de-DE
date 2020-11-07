---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azcurrentstorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Set-AzCurrentStorageAccount.md
ms.openlocfilehash: 87a24efbd5fca423d700ab01dd78765fd6d595bc
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/16/2020
ms.locfileid: "93842899"
---
# <span data-ttu-id="cec31-101">Set-AzCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cec31-101">Set-AzCurrentStorageAccount</span></span>

## <span data-ttu-id="cec31-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="cec31-102">SYNOPSIS</span></span>
<span data-ttu-id="cec31-103">Ändert das aktuelle Speicherkonto des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="cec31-103">Modifies the current Storage account of the specified subscription.</span></span>

## <span data-ttu-id="cec31-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="cec31-104">SYNTAX</span></span>

### <span data-ttu-id="cec31-105">UsingResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="cec31-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="cec31-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="cec31-106">UsingStorageContext</span></span>
```
Set-AzCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="cec31-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cec31-107">DESCRIPTION</span></span>
<span data-ttu-id="cec31-108">Das Cmdlet " **Satz-AzCurrentStorageAccount** " ändert das aktuelle Azure-Speicherkonto des angegebenen Azure-Abonnements in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="cec31-108">The **Set-AzCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="cec31-109">Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf den Speicher zugreifen, ohne einen Speicherkonto Namen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="cec31-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="cec31-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="cec31-110">EXAMPLES</span></span>

### <span data-ttu-id="cec31-111">Beispiel 1: Einrichten des aktuellen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="cec31-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="cec31-112">Dieser Befehl legt das Standardspeicher Konto für das angegebene Abonnement fest.</span><span class="sxs-lookup"><span data-stu-id="cec31-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="cec31-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="cec31-113">PARAMETERS</span></span>

### <span data-ttu-id="cec31-114">-Context</span><span class="sxs-lookup"><span data-stu-id="cec31-114">-Context</span></span>
<span data-ttu-id="cec31-115">Gibt ein **AzureStorageContext** -Objekt für das aktuelle Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="cec31-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="cec31-116">Verwenden Sie zum Abrufen eines Speicherkontext Objekts das New-AzStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cec31-116">To obtain a storage context object, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="cec31-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cec31-117">-DefaultProfile</span></span>
<span data-ttu-id="cec31-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="cec31-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="cec31-119">-Name</span><span class="sxs-lookup"><span data-stu-id="cec31-119">-Name</span></span>
<span data-ttu-id="cec31-120">Gibt den Namen des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="cec31-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="cec31-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cec31-121">-ResourceGroupName</span></span>
<span data-ttu-id="cec31-122">Gibt die Ressourcengruppe an, die das zu ändernde Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="cec31-122">Specifies the resource group that contains the Storage account to modify.</span></span>

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

### <span data-ttu-id="cec31-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cec31-123">CommonParameters</span></span>
<span data-ttu-id="cec31-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cec31-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cec31-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cec31-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cec31-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="cec31-126">INPUTS</span></span>

### <span data-ttu-id="cec31-127">Microsoft. Azure. Commands. Common. Authentication. Abstractions. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="cec31-127">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

### <span data-ttu-id="cec31-128">System. String</span><span class="sxs-lookup"><span data-stu-id="cec31-128">System.String</span></span>

## <span data-ttu-id="cec31-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="cec31-129">OUTPUTS</span></span>

### <span data-ttu-id="cec31-130">System. String</span><span class="sxs-lookup"><span data-stu-id="cec31-130">System.String</span></span>

## <span data-ttu-id="cec31-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="cec31-131">NOTES</span></span>

## <span data-ttu-id="cec31-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="cec31-132">RELATED LINKS</span></span>

[<span data-ttu-id="cec31-133">Satz-AzStorageAccount</span><span class="sxs-lookup"><span data-stu-id="cec31-133">Set-AzStorageAccount</span></span>](./Set-AzStorageAccount.md)


