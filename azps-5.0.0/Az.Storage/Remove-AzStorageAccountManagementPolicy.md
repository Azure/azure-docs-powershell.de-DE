---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94179533"
---
# <span data-ttu-id="5e00c-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="5e00c-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="5e00c-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="5e00c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e00c-103">Entfernt die Verwaltungsrichtlinie eines Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5e00c-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="5e00c-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="5e00c-104">SYNTAX</span></span>

### <span data-ttu-id="5e00c-105">Kontoname (Standard)</span><span class="sxs-lookup"><span data-stu-id="5e00c-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e00c-106">Kontoobject</span><span class="sxs-lookup"><span data-stu-id="5e00c-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e00c-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5e00c-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5e00c-108">Richtlinienobject</span><span class="sxs-lookup"><span data-stu-id="5e00c-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5e00c-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5e00c-109">DESCRIPTION</span></span>
<span data-ttu-id="5e00c-110">Das Cmdlet **Remove-AzStorageAccountManagementPolicy** entfernt die Verwaltungsrichtlinie eines Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="5e00c-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="5e00c-111">Beispiele</span><span class="sxs-lookup"><span data-stu-id="5e00c-111">EXAMPLES</span></span>

### <span data-ttu-id="5e00c-112">Beispiel 1: Entfernen der Verwaltungsrichtlinie eines speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e00c-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="5e00c-113">Mit diesem Befehl wird die Verwaltungsrichtlinie eines speicherkontos entfernt.</span><span class="sxs-lookup"><span data-stu-id="5e00c-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="5e00c-114">Parameter</span><span class="sxs-lookup"><span data-stu-id="5e00c-114">PARAMETERS</span></span>

### <span data-ttu-id="5e00c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5e00c-115">-DefaultProfile</span></span>
<span data-ttu-id="5e00c-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="5e00c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5e00c-117">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="5e00c-117">-InputObject</span></span>
<span data-ttu-id="5e00c-118">Zu entfernendes Verwaltungsobjekt</span><span class="sxs-lookup"><span data-stu-id="5e00c-118">Management Object to Remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSManagementPolicy
Parameter Sets: PolicyObject
Aliases: ManagementPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5e00c-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5e00c-119">-PassThru</span></span>
<span data-ttu-id="5e00c-120">Gibt an, dass dieses Cmdlet einen **booleschen Wert** zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="5e00c-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="5e00c-121">Standardmäßig gibt dieses Cmdlet keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="5e00c-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="5e00c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5e00c-122">-ResourceGroupName</span></span>
<span data-ttu-id="5e00c-123">Name der Ressourcengruppe.</span><span class="sxs-lookup"><span data-stu-id="5e00c-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5e00c-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="5e00c-124">-StorageAccount</span></span>
<span data-ttu-id="5e00c-125">Speicherkonto Objekt</span><span class="sxs-lookup"><span data-stu-id="5e00c-125">Storage account object</span></span>

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

### <span data-ttu-id="5e00c-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5e00c-126">-StorageAccountName</span></span>
<span data-ttu-id="5e00c-127">Name des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e00c-127">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5e00c-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="5e00c-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="5e00c-129">Ressourcen-ID des speicherkontos</span><span class="sxs-lookup"><span data-stu-id="5e00c-129">Storage Account Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e00c-130">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="5e00c-130">-Confirm</span></span>
<span data-ttu-id="5e00c-131">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="5e00c-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5e00c-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5e00c-132">-WhatIf</span></span>
<span data-ttu-id="5e00c-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5e00c-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5e00c-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="5e00c-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5e00c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e00c-135">CommonParameters</span></span>
<span data-ttu-id="5e00c-136">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5e00c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e00c-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e00c-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e00c-138">Eingaben</span><span class="sxs-lookup"><span data-stu-id="5e00c-138">INPUTS</span></span>

### <span data-ttu-id="5e00c-139">System. String</span><span class="sxs-lookup"><span data-stu-id="5e00c-139">System.String</span></span>

## <span data-ttu-id="5e00c-140">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="5e00c-140">OUTPUTS</span></span>

### <span data-ttu-id="5e00c-141">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="5e00c-141">System.Boolean</span></span>

## <span data-ttu-id="5e00c-142">Notizen</span><span class="sxs-lookup"><span data-stu-id="5e00c-142">NOTES</span></span>

## <span data-ttu-id="5e00c-143">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="5e00c-143">RELATED LINKS</span></span>
