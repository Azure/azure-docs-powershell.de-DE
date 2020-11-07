---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
ms.assetid: 15973FE8-16C1-4B71-A3A8-6D6F67A96FDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/set-azurermcurrentstorageaccount
schema: 2.0.0
ms.openlocfilehash: 6a7ef50e6e95a30140549343d14d4a75ad340cbc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93663741"
---
# <span data-ttu-id="09097-101">Set-AzureRmCurrentStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09097-101">Set-AzureRmCurrentStorageAccount</span></span>

## <span data-ttu-id="09097-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="09097-102">SYNOPSIS</span></span>
<span data-ttu-id="09097-103">Ändert das aktuelle Speicherkonto des angegebenen Abonnements.</span><span class="sxs-lookup"><span data-stu-id="09097-103">Modifies the current Storage account of the specified subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="09097-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="09097-104">SYNTAX</span></span>

### <span data-ttu-id="09097-105">UsingResourceGroupAndNameParameterSet (Standard)</span><span class="sxs-lookup"><span data-stu-id="09097-105">UsingResourceGroupAndNameParameterSet (Default)</span></span>
```
Set-AzureRmCurrentStorageAccount -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09097-106">UsingStorageContext</span><span class="sxs-lookup"><span data-stu-id="09097-106">UsingStorageContext</span></span>
```
Set-AzureRmCurrentStorageAccount -Context <IStorageContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="09097-107">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09097-107">DESCRIPTION</span></span>
<span data-ttu-id="09097-108">Das Cmdlet " **Satz-AzureRmCurrentStorageAccount** " ändert das aktuelle Azure-Speicherkonto des angegebenen Azure-Abonnements in Azure PowerShell.</span><span class="sxs-lookup"><span data-stu-id="09097-108">The **Set-AzureRmCurrentStorageAccount** cmdlet modifies the current Azure Storage account of the specified Azure subscription in Azure PowerShell.</span></span>
<span data-ttu-id="09097-109">Das aktuelle Speicherkonto wird als Standard verwendet, wenn Sie auf den Speicher zugreifen, ohne einen Speicherkonto Namen anzugeben.</span><span class="sxs-lookup"><span data-stu-id="09097-109">The current Storage account is used as the default when you access Storage without specifying a Storage account name.</span></span>

## <span data-ttu-id="09097-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="09097-110">EXAMPLES</span></span>

### <span data-ttu-id="09097-111">Beispiel 1: Einrichten des aktuellen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="09097-111">Example 1: Set the current Storage account</span></span>
```
PS C:\>Set-AzureRmCurrentStorageAccount -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="09097-112">Dieser Befehl legt das Standardspeicher Konto für das angegebene Abonnement fest.</span><span class="sxs-lookup"><span data-stu-id="09097-112">This command sets the default Storage account for the specified subscription.</span></span>

## <span data-ttu-id="09097-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="09097-113">PARAMETERS</span></span>

### <span data-ttu-id="09097-114">-Context</span><span class="sxs-lookup"><span data-stu-id="09097-114">-Context</span></span>
<span data-ttu-id="09097-115">Gibt ein **AzureStorageContext** -Objekt für das aktuelle Speicherkonto an.</span><span class="sxs-lookup"><span data-stu-id="09097-115">Specifies an **AzureStorageContext** object for the current Storage account.</span></span>
<span data-ttu-id="09097-116">Verwenden Sie zum Abrufen eines Speicherkontext Objekts das New-AzureStorageContext-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="09097-116">To obtain a storage context object, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: UsingStorageContext
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09097-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09097-117">-DefaultProfile</span></span>
<span data-ttu-id="09097-118">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="09097-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09097-119">-Name</span><span class="sxs-lookup"><span data-stu-id="09097-119">-Name</span></span>
<span data-ttu-id="09097-120">Gibt den Namen des speicherkontos an, das von diesem Cmdlet geändert wird.</span><span class="sxs-lookup"><span data-stu-id="09097-120">Specifies the name of the Storage account that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: StorageAccountName, AccountName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09097-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="09097-121">-ResourceGroupName</span></span>
<span data-ttu-id="09097-122">Gibt die Ressourcengruppe an, die das zu ändernde Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="09097-122">Specifies the resource group that contains the Storage account to modify.</span></span>

```yaml
Type: String
Parameter Sets: UsingResourceGroupAndNameParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="09097-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09097-123">CommonParameters</span></span>
<span data-ttu-id="09097-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="09097-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09097-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="09097-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09097-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="09097-126">INPUTS</span></span>

### <span data-ttu-id="09097-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="09097-127">IStorageContext</span></span>
<span data-ttu-id="09097-128">Der Parameter "Context" akzeptiert den Wert vom Typ "IStorageContext" aus der Pipeline.</span><span class="sxs-lookup"><span data-stu-id="09097-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="09097-129">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="09097-129">OUTPUTS</span></span>

### <span data-ttu-id="09097-130">System. String</span><span class="sxs-lookup"><span data-stu-id="09097-130">System.String</span></span>

## <span data-ttu-id="09097-131">Notizen</span><span class="sxs-lookup"><span data-stu-id="09097-131">NOTES</span></span>

## <span data-ttu-id="09097-132">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="09097-132">RELATED LINKS</span></span>

[<span data-ttu-id="09097-133">Satz-AzureRmStorageAccount</span><span class="sxs-lookup"><span data-stu-id="09097-133">Set-AzureRmStorageAccount</span></span>](./Set-AzureRmStorageAccount.md)


