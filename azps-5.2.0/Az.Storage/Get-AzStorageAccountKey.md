---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
ms.assetid: A57A9EFA-47AC-44D8-BFA7-CDE0E2A612B3
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageAccountKey.md
ms.openlocfilehash: 3a681f2df128979ad79d678101b400b040fa994c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98290614"
---
# <span data-ttu-id="c1a1b-101">Get-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c1a1b-101">Get-AzStorageAccountKey</span></span>

## <span data-ttu-id="c1a1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1a1b-102">SYNOPSIS</span></span>
<span data-ttu-id="c1a1b-103">Ruft die Zugriffstasten für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-103">Gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="c1a1b-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c1a1b-104">SYNTAX</span></span>

```
Get-AzStorageAccountKey [-ResourceGroupName] <String> [-Name] <String> [-ListKerbKey]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1a1b-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c1a1b-105">DESCRIPTION</span></span>
<span data-ttu-id="c1a1b-106">Das **Cmdlet "Get-AzStorageAccountKey"** ruft die Zugriffsschlüssel für ein Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-106">The **Get-AzStorageAccountKey** cmdlet gets the access keys for an Azure Storage account.</span></span>

## <span data-ttu-id="c1a1b-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c1a1b-107">EXAMPLES</span></span>

### <span data-ttu-id="c1a1b-108">Beispiel 1: Erhalten der Zugriffstasten für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c1a1b-108">Example 1: Get the access keys for a Storage account</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount"
```

<span data-ttu-id="c1a1b-109">Dieser Befehl ruft die Schlüssel für das angegebene Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-109">This command gets the keys for the specified Azure Storage account.</span></span>

### <span data-ttu-id="c1a1b-110">Beispiel 2: Erhalten eines bestimmten Zugriffsschlüssels für ein Speicherkonto</span><span class="sxs-lookup"><span data-stu-id="c1a1b-110">Example 2: Get a specific access key for a Storage account</span></span>
```
This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.4, and later versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount")| Where-Object {$_.KeyName -eq "key1"}

This command gets a specific key for a Storage account. This command works for Azure PowerShell version 1.3.2, and previous versions.
PS C:\>(Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount").Key1
```

### <span data-ttu-id="c1a1b-111">Beispiel 3: Listet die Zugriffstasten für ein Speicherkonto auf, enthält die Kerberos-Schlüssel (wenn Active Directory aktiviert ist)</span><span class="sxs-lookup"><span data-stu-id="c1a1b-111">Example 3: Lists the access keys for a Storage account, include the Kerberos keys (if active directory enabled)</span></span>
```
PS C:\>Get-AzStorageAccountKey -ResourceGroupName "RG01" -AccountName "mystorageaccount" -ListKerbKey
```

<span data-ttu-id="c1a1b-112">Dieser Befehl ruft die Schlüssel für das angegebene Azure Storage-Konto ab.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-112">This command gets the keys for the specified Azure Storage account.</span></span>

## <span data-ttu-id="c1a1b-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c1a1b-113">PARAMETERS</span></span>

### <span data-ttu-id="c1a1b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1a1b-114">-DefaultProfile</span></span>
<span data-ttu-id="c1a1b-115">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c1a1b-116">-ListKerbKey</span><span class="sxs-lookup"><span data-stu-id="c1a1b-116">-ListKerbKey</span></span>
<span data-ttu-id="c1a1b-117">Listet die Kerberos-Schlüssel (wenn Active Directory aktiviert ist) für das angegebene Speicherkonto auf.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-117">Lists the Kerberos keys (if active directory enabled) for the specified storage account.</span></span>
<span data-ttu-id="c1a1b-118">Der Kerberos-Schlüssel wird pro Speicherkonto für die identitätsbasierte Authentifizierung in Azure Files entweder mit Azure Active Directory Domain Service (Azure AD DS) oder Active Directory Domain Service (AD DS) generiert.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-118">Kerberos key is generated per storage account for Azure Files identity based authentication either with Azure Active Directory Domain Service (Azure AD DS) or Active Directory Domain Service (AD DS).</span></span> <span data-ttu-id="c1a1b-119">Es wird als Kennwort der Identität verwendet, die im Domänendienst registriert ist, der das Speicherkonto darstellt.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-119">It is used as the password of the identity registered in the domain service that represents the storage account.</span></span> <span data-ttu-id="c1a1b-120">Der Kerberos Key bietet keine Zugriffsberechtigungen zum Ausführen von Steuerelement- oder Datenebenen-Lese- oder -Schreibvorgängen für das Speicherkonto.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-120">Kerberos key does not provide access permission to perform any control or data plane read or write operations against the storage account.</span></span>

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

### <span data-ttu-id="c1a1b-121">-Name</span><span class="sxs-lookup"><span data-stu-id="c1a1b-121">-Name</span></span>
<span data-ttu-id="c1a1b-122">Gibt den Namen des Speicherkontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-122">Specifies the name of the Storage account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="c1a1b-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c1a1b-123">-ResourceGroupName</span></span>
<span data-ttu-id="c1a1b-124">Gibt den Namen der Ressourcengruppe an, die das Speicherkonto enthält.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-124">Specifies the name of the resource group that contains the Storage account.</span></span>

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

### <span data-ttu-id="c1a1b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1a1b-125">CommonParameters</span></span>
<span data-ttu-id="c1a1b-126">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c1a1b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1a1b-127">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c1a1b-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1a1b-128">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c1a1b-128">INPUTS</span></span>

### <span data-ttu-id="c1a1b-129">System.String</span><span class="sxs-lookup"><span data-stu-id="c1a1b-129">System.String</span></span>

## <span data-ttu-id="c1a1b-130">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c1a1b-130">OUTPUTS</span></span>

### <span data-ttu-id="c1a1b-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c1a1b-131">Microsoft.Azure.Management.Storage.Models.StorageAccountKey</span></span>

## <span data-ttu-id="c1a1b-132">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c1a1b-132">NOTES</span></span>

## <span data-ttu-id="c1a1b-133">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c1a1b-133">RELATED LINKS</span></span>

[<span data-ttu-id="c1a1b-134">New-AzStorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="c1a1b-134">New-AzStorageAccountKey</span></span>](./New-AzStorageAccountKey.md)


