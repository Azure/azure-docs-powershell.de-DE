---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstoragefileserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageFileServiceProperty.md
ms.openlocfilehash: 0824045a6b916d34a7b268c32e9667e954a4e1e5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94176554"
---
# <span data-ttu-id="36093-101">Get-AzStorageFileServiceProperty</span><span class="sxs-lookup"><span data-stu-id="36093-101">Get-AzStorageFileServiceProperty</span></span>

## <span data-ttu-id="36093-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="36093-102">SYNOPSIS</span></span>
<span data-ttu-id="36093-103">Ruft Diensteigenschaften für Azure Storage-Dateidienste ab.</span><span class="sxs-lookup"><span data-stu-id="36093-103">Gets service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="36093-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="36093-104">SYNTAX</span></span>

### <span data-ttu-id="36093-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="36093-105">AccountName (Default)</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="36093-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="36093-106">AccountObject</span></span>
```
Get-AzStorageFileServiceProperty -StorageAccount <PSStorageAccount> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="36093-107">FileServicePropertiesResourceId</span><span class="sxs-lookup"><span data-stu-id="36093-107">FileServicePropertiesResourceId</span></span>
```
Get-AzStorageFileServiceProperty [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="36093-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="36093-108">DESCRIPTION</span></span>
<span data-ttu-id="36093-109">Das Cmdlet " **Get-AzStorageFileServiceProperty** " Ruft die Diensteigenschaften für Azure Storage-Dateidienste ab.</span><span class="sxs-lookup"><span data-stu-id="36093-109">The **Get-AzStorageFileServiceProperty** cmdlet gets the service properties for Azure Storage File services.</span></span>

## <span data-ttu-id="36093-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="36093-110">EXAMPLES</span></span>

### <span data-ttu-id="36093-111">Beispiel 1: Abrufen der Azure Storage File Services-Eigenschaft eines angegebenen speicherkontos</span><span class="sxs-lookup"><span data-stu-id="36093-111">Example 1: Get  Azure Storage File services property of a specified Storage Account</span></span>
```powershell
PS C:\> Get-AzStorageFileServiceProperty -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"

StorageAccountName ResourceGroupName ShareDeleteRetentionPolicy.Enabled ShareDeleteRetentionPolicy.Days
------------------ ----------------- ---------------------------------- -------------------------------
mystorageaccount   myresourcegroup   True                               5
```

<span data-ttu-id="36093-112">Dieser Befehl ruft die Eigenschaft "Dateidienste" eines angegebenen speicherkontos ab.</span><span class="sxs-lookup"><span data-stu-id="36093-112">This command gets the File services property of a specified Storage Account.</span></span>

## <span data-ttu-id="36093-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="36093-113">PARAMETERS</span></span>

### <span data-ttu-id="36093-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="36093-114">-DefaultProfile</span></span>
<span data-ttu-id="36093-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="36093-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="36093-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="36093-116">-ResourceGroupName</span></span>
<span data-ttu-id="36093-117">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="36093-117">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36093-118">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="36093-118">-ResourceId</span></span>
<span data-ttu-id="36093-119">Geben Sie eine Ressourcen-ID des speicherkontos oder eine Ressourcen-ID für Dateidienst Eigenschaften ein.</span><span class="sxs-lookup"><span data-stu-id="36093-119">Input a Storage account Resource Id, or a File service properties Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: FileServicePropertiesResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="36093-120">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="36093-120">-StorageAccount</span></span>
<span data-ttu-id="36093-121">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="36093-121">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="36093-122">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="36093-122">-StorageAccountName</span></span>
<span data-ttu-id="36093-123">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="36093-123">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName, Name

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="36093-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="36093-124">CommonParameters</span></span>
<span data-ttu-id="36093-125">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="36093-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="36093-126">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="36093-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="36093-127">Eingaben</span><span class="sxs-lookup"><span data-stu-id="36093-127">INPUTS</span></span>

### <span data-ttu-id="36093-128">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="36093-128">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="36093-129">System. String</span><span class="sxs-lookup"><span data-stu-id="36093-129">System.String</span></span>

## <span data-ttu-id="36093-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="36093-130">OUTPUTS</span></span>

### <span data-ttu-id="36093-131">Microsoft. Azure. Commands. Management. Storage. Models. PSFileServiceProperties</span><span class="sxs-lookup"><span data-stu-id="36093-131">Microsoft.Azure.Commands.Management.Storage.Models.PSFileServiceProperties</span></span>

## <span data-ttu-id="36093-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="36093-132">NOTES</span></span>

## <span data-ttu-id="36093-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="36093-133">RELATED LINKS</span></span>
