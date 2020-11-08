---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179968"
---
# <span data-ttu-id="f6ebf-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6ebf-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="f6ebf-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="f6ebf-102">SYNOPSIS</span></span>
<span data-ttu-id="f6ebf-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f6ebf-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="f6ebf-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6ebf-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f6ebf-105">DESCRIPTION</span></span>
<span data-ttu-id="f6ebf-106">Das Cmdlet " **Get-AzStorageAccountKey** " Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="f6ebf-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="f6ebf-107">EXAMPLES</span></span>

### <span data-ttu-id="f6ebf-108">Beispiel 1: Abrufen der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f6ebf-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="f6ebf-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="f6ebf-110">Beispiel 2: Abrufen einer bestimmten Zugriffstaste für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="f6ebf-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="f6ebf-111">Beispiel 3: Listet die Zugriffstasten für ein Speicherkonto auf, einschließlich der Kerberos-Schlüssel (wenn Active Directory aktiviert ist)</span><span class="sxs-lookup"><span data-stu-id="f6ebf-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="f6ebf-112">Dieser Befehl ruft die Schlüssel für das angegebene Azure-Speicherkonto ab.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="f6ebf-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="f6ebf-113">PARAMETERS</span></span>

### <span data-ttu-id="f6ebf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6ebf-114">-DefaultProfile</span></span>
<span data-ttu-id="f6ebf-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6ebf-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="f6ebf-116">-ListKerbKey</span></span>
<span data-ttu-id="f6ebf-117">Listet die Kerberos-Schlüssel (wenn Active Directory aktiviert ist) für das angegebene Speicherkonto auf.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="f6ebf-118">Der Kerberos-Schlüssel wird pro Speicherkonto für Azure Identity-basierte Authentifizierung entweder mit Azure Active Directory-Domänendienst (Azure AD DS) oder Active Directory-Domänendienst (AD DS) generiert.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="f6ebf-119">Sie wird als Kennwort der im Domänendienst registrierten Identität verwendet, die das Speicherkonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="f6ebf-120">Der Kerberos-Schlüssel bietet keine Zugriffsberechtigung, um Steuerelemente oder Datenebenen-Lese-oder Schreibvorgänge für das Speicherkonto durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6ebf-121">-Name</span><span class="sxs-lookup"><span data-stu-id="f6ebf-121">-Name</span></span>
<span data-ttu-id="f6ebf-122">Gibt den Namen des speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="f6ebf-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f6ebf-123">-ResourceGroupName</span></span>
<span data-ttu-id="f6ebf-124">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="f6ebf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6ebf-125">CommonParameters</span></span>
<span data-ttu-id="f6ebf-126">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f6ebf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6ebf-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6ebf-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6ebf-128">Eingaben</span><span class="sxs-lookup"><span data-stu-id="f6ebf-128">INPUTS</span></span>

### <span data-ttu-id="f6ebf-129">System. String</span><span class="sxs-lookup"><span data-stu-id="f6ebf-129">System.String</span></span>

## <span data-ttu-id="f6ebf-130">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="f6ebf-130">OUTPUTS</span></span>

### <span data-ttu-id="f6ebf-131">Microsoft. Azure. Management. Storage. Models. StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6ebf-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="f6ebf-132">Notizen</span><span class="sxs-lookup"><span data-stu-id="f6ebf-132">NOTES</span></span>

## <span data-ttu-id="f6ebf-133">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="f6ebf-133">RELATED LINKS</span></span>

[<span data-ttu-id="f6ebf-134">Neu – AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="f6ebf-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


