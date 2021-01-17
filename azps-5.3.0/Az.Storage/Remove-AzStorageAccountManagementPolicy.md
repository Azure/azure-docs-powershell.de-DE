---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storage/remove-Azstorageaccountmanagementpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzStorageAccountManagementPolicy.md
ms.openlocfilehash: 6f4907f9ee94c05161fa602fc5cefd0ead4f6224
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/05/2021
ms.locfileid: "98460244"
---
# <span data-ttu-id="01bdf-101">Remove-AzStorageAccountManagementPolicy</span><span class="sxs-lookup"><span data-stu-id="01bdf-101">Remove-AzStorageAccountManagementPolicy</span></span>

## <span data-ttu-id="01bdf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01bdf-102">SYNOPSIS</span></span>
<span data-ttu-id="01bdf-103">Entfernt die Verwaltungsrichtlinie eines Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="01bdf-103">Removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="01bdf-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="01bdf-104">SYNTAX</span></span>

### <span data-ttu-id="01bdf-105">AccountName (Standard)</span><span class="sxs-lookup"><span data-stu-id="01bdf-105">AccountName (Default)</span></span>
```
Remove-AzStorageAccountManagementPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01bdf-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="01bdf-106">AccountObject</span></span>
```
Remove-AzStorageAccountManagementPolicy -StorageAccount <PSStorageAccount> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01bdf-107">AccountResourceId</span><span class="sxs-lookup"><span data-stu-id="01bdf-107">AccountResourceId</span></span>
```
Remove-AzStorageAccountManagementPolicy [-StorageAccountResourceId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="01bdf-108">PolicyObject</span><span class="sxs-lookup"><span data-stu-id="01bdf-108">PolicyObject</span></span>
```
Remove-AzStorageAccountManagementPolicy [-InputObject] <PSManagementPolicy> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="01bdf-109">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="01bdf-109">DESCRIPTION</span></span>
<span data-ttu-id="01bdf-110">Das **Cmdlet "Remove-AzStorageAccountManagementPolicy"** entfernt die Verwaltungsrichtlinie eines Azure Storage-Kontos.</span><span class="sxs-lookup"><span data-stu-id="01bdf-110">The **Remove-AzStorageAccountManagementPolicy** cmdlet removes the management policy of an Azure Storage account.</span></span>

## <span data-ttu-id="01bdf-111">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="01bdf-111">EXAMPLES</span></span>

### <span data-ttu-id="01bdf-112">Beispiel 1: Entfernen der Verwaltungsrichtlinie eines Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="01bdf-112">Example 1: Remove the management policy of a Storage account.</span></span>
```
PS C:\>Remove-AzStorageAccountManagementPolicy -ResourceGroupName "MyResourceGroup" -AccountName "mystorageaccount"
```

<span data-ttu-id="01bdf-113">Mit diesem Befehl wird die Verwaltungsrichtlinie eines Speicherkontos entfernt.</span><span class="sxs-lookup"><span data-stu-id="01bdf-113">This command removes the management policy of a Storage account.</span></span>

## <span data-ttu-id="01bdf-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="01bdf-114">PARAMETERS</span></span>

### <span data-ttu-id="01bdf-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01bdf-115">-DefaultProfile</span></span>
<span data-ttu-id="01bdf-116">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01bdf-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01bdf-117">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01bdf-117">-InputObject</span></span>
<span data-ttu-id="01bdf-118">Zu entfernende Verwaltungsobjekt</span><span class="sxs-lookup"><span data-stu-id="01bdf-118">Management Object to Remove</span></span>

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

### <span data-ttu-id="01bdf-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="01bdf-119">-PassThru</span></span>
<span data-ttu-id="01bdf-120">Gibt an, dass dieses Cmdlet einen **booleschen** Wert zurückgibt, der den Erfolg des Vorgangs widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="01bdf-120">Indicates that this cmdlet returns a **Boolean** that reflects the success of the operation.</span></span>
<span data-ttu-id="01bdf-121">Dieses Cmdlet gibt standardmäßig keinen Wert zurück.</span><span class="sxs-lookup"><span data-stu-id="01bdf-121">By default, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="01bdf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01bdf-122">-ResourceGroupName</span></span>
<span data-ttu-id="01bdf-123">Ressourcengruppenname.</span><span class="sxs-lookup"><span data-stu-id="01bdf-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="01bdf-124">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="01bdf-124">-StorageAccount</span></span>
<span data-ttu-id="01bdf-125">Speicherkontoobjekt</span><span class="sxs-lookup"><span data-stu-id="01bdf-125">Storage account object</span></span>

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

### <span data-ttu-id="01bdf-126">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="01bdf-126">-StorageAccountName</span></span>
<span data-ttu-id="01bdf-127">Speicherkontoname.</span><span class="sxs-lookup"><span data-stu-id="01bdf-127">Storage Account Name.</span></span>

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

### <span data-ttu-id="01bdf-128">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="01bdf-128">-StorageAccountResourceId</span></span>
<span data-ttu-id="01bdf-129">Ressourcen-ID des Speicherkontos.</span><span class="sxs-lookup"><span data-stu-id="01bdf-129">Storage Account Resource Id.</span></span>

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

### <span data-ttu-id="01bdf-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="01bdf-130">-Confirm</span></span>
<span data-ttu-id="01bdf-131">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="01bdf-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01bdf-132">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="01bdf-132">-WhatIf</span></span>
<span data-ttu-id="01bdf-133">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="01bdf-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01bdf-134">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="01bdf-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01bdf-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01bdf-135">CommonParameters</span></span>
<span data-ttu-id="01bdf-136">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="01bdf-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01bdf-137">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01bdf-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01bdf-138">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="01bdf-138">INPUTS</span></span>

### <span data-ttu-id="01bdf-139">System.String</span><span class="sxs-lookup"><span data-stu-id="01bdf-139">System.String</span></span>

## <span data-ttu-id="01bdf-140">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="01bdf-140">OUTPUTS</span></span>

### <span data-ttu-id="01bdf-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="01bdf-141">System.Boolean</span></span>

## <span data-ttu-id="01bdf-142">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="01bdf-142">NOTES</span></span>

## <span data-ttu-id="01bdf-143">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="01bdf-143">RELATED LINKS</span></span>
