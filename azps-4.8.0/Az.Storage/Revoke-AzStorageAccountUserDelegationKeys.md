---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/revoke-azstorageaccountuserdelegationkeys
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Revoke-AzStorageAccountUserDelegationKeys.md
ms.openlocfilehash: f6f12358e3182796f7665db4ee0b45cf42ea2c66
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/13/2020
ms.locfileid: "94165965"
---
# <span data-ttu-id="5dd7c-101">Revoke-AzStorageAccountUserDelegationKeys</span><span class="sxs-lookup"><span data-stu-id="5dd7c-101">Revoke-AzStorageAccountUserDelegationKeys</span></span>

## <span data-ttu-id="5dd7c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5dd7c-102">SYNOPSIS</span></span>
<span data-ttu-id="5dd7c-103">Alle Benutzer Delegierungs Schlüssel eines speicherkontos widerrufen.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-103">Revoke all User Delegation keys of a Storage account.</span></span>

## <span data-ttu-id="5dd7c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5dd7c-104">SYNTAX</span></span>

### <span data-ttu-id="5dd7c-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="5dd7c-105">AccountName (Default)</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd7c-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="5dd7c-106">AccountObject</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys -InputObject <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5dd7c-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5dd7c-107">AccountResourceId</span></span>
```
Revoke-AzStorageAccountUserDelegationKeys [-ResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5dd7c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5dd7c-108">DESCRIPTION</span></span>
<span data-ttu-id="5dd7c-109">Das **REVOKE-AzStorageAccountUserDelegationKeys-** Cmdlet hebt alle Benutzer Delegierungs Schlüssel eines speicherkontos auf, damit das gesamte Identity SAS-Token des speicherkontos ebenfalls gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-109">The **Revoke-AzStorageAccountUserDelegationKeys** cmdlet revokes all User Delegation keys of a Storage account, so all Identity SAS token of the Storage account will also be revoked.</span></span>

## <span data-ttu-id="5dd7c-110">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5dd7c-110">EXAMPLES</span></span>

### <span data-ttu-id="5dd7c-111">Beispiel 1: widerrufen aller Benutzer Delegierungs Schlüssel eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5dd7c-111">Example 1: Revoke all User Delegation keys of a Storage account</span></span>
```powershell
PS C:\>Revoke-AzStorageAccountUserDelegationKeys -ResourceGroupName "myresourcegroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="5dd7c-112">In diesem Beispiel werden alle Benutzer Delegierungs Schlüssel eines speicherkontos aufgehoben, sodass alle aus den Benutzer Delegierungs Schlüsseln generierten Identity SAS-Token ebenfalls widerrufen werden.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-112">This example revokes all User Delegation keys of a Storage account, so all Identity SAS token generated from the User Delegation keys will also be revoked.</span></span>

## <span data-ttu-id="5dd7c-113">Parameter</span><span class="sxs-lookup"><span data-stu-id="5dd7c-113">PARAMETERS</span></span>

### <span data-ttu-id="5dd7c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dd7c-114">-DefaultProfile</span></span>
<span data-ttu-id="5dd7c-115">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dd7c-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5dd7c-116">-InputObject</span></span>
<span data-ttu-id="5dd7c-117">Ein Speicherkonto Objekt, das von Get_AzStorageAccount, New-AzStorageAccount, zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-117">A storage account object, returned by Get_AzStorageAccount, New-AzStorageAccount.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases: StorageAccount

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd7c-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5dd7c-118">-PassThru</span></span>
<span data-ttu-id="5dd7c-119">In der Regel gibt dieses Cmdlet beim erfolgreichen Abschluss keine Ausgabe zurück, und dieser Parameter erzwingt, dass das Cmdlet beim erfolgreichen Abschluss einen Wert ($true) zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-119">Normally this cmdlet returns no output on successful completion, this parameter forces the cmdlet to return a value ($true) on successful completion.</span></span>

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

### <span data-ttu-id="5dd7c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dd7c-120">-ResourceGroupName</span></span>
<span data-ttu-id="5dd7c-121">Der Name der Ressourcengruppe, die die Speicherkonto Ressource enthält.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-121">The resource group name containing the storage account resource.</span></span>

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

### <span data-ttu-id="5dd7c-122">-Resourcen-Nr</span><span class="sxs-lookup"><span data-stu-id="5dd7c-122">-ResourceId</span></span>
<span data-ttu-id="5dd7c-123">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5dd7c-123">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases: StorageAccountResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dd7c-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5dd7c-124">-StorageAccountName</span></span>
<span data-ttu-id="5dd7c-125">Der Name der Speicherkonto Ressource.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-125">The name of the storage account resource.</span></span>

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

### <span data-ttu-id="5dd7c-126">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5dd7c-126">-Confirm</span></span>
<span data-ttu-id="5dd7c-127">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd7c-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dd7c-128">-WhatIf</span></span>
<span data-ttu-id="5dd7c-129">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dd7c-130">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dd7c-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dd7c-131">CommonParameters</span></span>
<span data-ttu-id="5dd7c-132">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5dd7c-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dd7c-133">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dd7c-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dd7c-134">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5dd7c-134">INPUTS</span></span>

### <span data-ttu-id="5dd7c-135">Microsoft. Azure. Commands. Management. Storage. Models. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5dd7c-135">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="5dd7c-136">System. String</span><span class="sxs-lookup"><span data-stu-id="5dd7c-136">System.String</span></span>

## <span data-ttu-id="5dd7c-137">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5dd7c-137">OUTPUTS</span></span>

### <span data-ttu-id="5dd7c-138">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5dd7c-138">System.Boolean</span></span>

## <span data-ttu-id="5dd7c-139">Notizen</span><span class="sxs-lookup"><span data-stu-id="5dd7c-139">NOTES</span></span>

## <span data-ttu-id="5dd7c-140">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5dd7c-140">RELATED LINKS</span></span>
