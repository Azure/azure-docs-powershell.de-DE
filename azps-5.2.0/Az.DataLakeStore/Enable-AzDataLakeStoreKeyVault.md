---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: c6d15769891f02a6c1be12a277e17ca2ccba107e
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 12/08/2020
ms.locfileid: "98371438"
---
# <span data-ttu-id="c5b18-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="c5b18-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="c5b18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5b18-102">SYNOPSIS</span></span>
<span data-ttu-id="c5b18-103">Versucht, einen vom Benutzer verwalteten Schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5b18-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c5b18-104">SYNTAX</span><span class="sxs-lookup"><span data-stu-id="c5b18-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c5b18-105">BESCHREIBUNG</span><span class="sxs-lookup"><span data-stu-id="c5b18-105">DESCRIPTION</span></span>
<span data-ttu-id="c5b18-106">Das **Cmdlet "Enable-AzDataLakeStoreKeyVault"** versucht, einen vom Benutzer verwalteten Schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5b18-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="c5b18-107">BEISPIELE</span><span class="sxs-lookup"><span data-stu-id="c5b18-107">EXAMPLES</span></span>

### <span data-ttu-id="c5b18-108">Beispiel 1: Aktivieren des Schlüsseltresor für das ContosoADLS-Konto</span><span class="sxs-lookup"><span data-stu-id="c5b18-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="c5b18-109">Mit diesem Befehl wird versucht, den vom Benutzer verwalteten Schlüsseltresor für das Data Lake Store-Konto namens ContosoADLS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c5b18-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="c5b18-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c5b18-110">PARAMETERS</span></span>

### <span data-ttu-id="c5b18-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="c5b18-111">-Account</span></span>
<span data-ttu-id="c5b18-112">Das Data Lake Store-Konto, um den vom Benutzer verwalteten Schlüsseltresor für</span><span class="sxs-lookup"><span data-stu-id="c5b18-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5b18-113">-DefaultProfile</span></span>
<span data-ttu-id="c5b18-114">Die Anmeldeinformationen, das Konto, den Mandanten und das Abonnement, die für die Kommunikation mit Azure verwendet werden</span><span class="sxs-lookup"><span data-stu-id="c5b18-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5b18-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5b18-115">-ResourceGroupName</span></span>
<span data-ttu-id="c5b18-116">Name der Ressourcengruppe, die dem Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c5b18-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="c5b18-117">Wenn nicht angegeben, wird versucht, erkannt zu werden.</span><span class="sxs-lookup"><span data-stu-id="c5b18-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5b18-118">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c5b18-118">-Confirm</span></span>
<span data-ttu-id="c5b18-119">Fordert Sie zur Bestätigung auf, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="c5b18-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c5b18-120">-Waswenn</span><span class="sxs-lookup"><span data-stu-id="c5b18-120">-WhatIf</span></span>
<span data-ttu-id="c5b18-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c5b18-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c5b18-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="c5b18-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c5b18-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5b18-123">CommonParameters</span></span>
<span data-ttu-id="c5b18-124">Dieses Cmdlet unterstützt die allgemeinen Parameter: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction und -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c5b18-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5b18-125">Weitere Informationen finden Sie unter about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5b18-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5b18-126">EINGABEN</span><span class="sxs-lookup"><span data-stu-id="c5b18-126">INPUTS</span></span>

### <span data-ttu-id="c5b18-127">System.String</span><span class="sxs-lookup"><span data-stu-id="c5b18-127">System.String</span></span>

## <span data-ttu-id="c5b18-128">AUSGABEN</span><span class="sxs-lookup"><span data-stu-id="c5b18-128">OUTPUTS</span></span>

### <span data-ttu-id="c5b18-129">System.Void</span><span class="sxs-lookup"><span data-stu-id="c5b18-129">System.Void</span></span>

## <span data-ttu-id="c5b18-130">HINWEISE</span><span class="sxs-lookup"><span data-stu-id="c5b18-130">NOTES</span></span>

## <span data-ttu-id="c5b18-131">LINKS ZU VERWANDTEN THEMEN</span><span class="sxs-lookup"><span data-stu-id="c5b18-131">RELATED LINKS</span></span>

[<span data-ttu-id="c5b18-132">New-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c5b18-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="c5b18-133">Set-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="c5b18-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

