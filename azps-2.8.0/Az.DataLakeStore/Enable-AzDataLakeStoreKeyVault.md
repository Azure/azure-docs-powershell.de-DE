---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeStore.dll-Help.xml
Module Name: Az.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakestore/enable-azdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeStore/DataLakeStore/help/Enable-AzDataLakeStoreKeyVault.md
ms.openlocfilehash: 0e8adfc9ef5cfd5525a0e07b35c3eb1b918b9ba7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 01/29/2020
ms.locfileid: "93651566"
---
# <span data-ttu-id="d3a79-101">Enable-AzDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="d3a79-101">Enable-AzDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="d3a79-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="d3a79-102">SYNOPSIS</span></span>
<span data-ttu-id="d3a79-103">Versucht, einen Benutzer verwalteten schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3a79-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d3a79-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="d3a79-104">SYNTAX</span></span>

```
Enable-AzDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3a79-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d3a79-105">DESCRIPTION</span></span>
<span data-ttu-id="d3a79-106">Das Cmdlet **enable-AzDataLakeStoreKeyVault** versucht, einen Benutzer verwalteten schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3a79-106">The **Enable-AzDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="d3a79-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="d3a79-107">EXAMPLES</span></span>

### <span data-ttu-id="d3a79-108">Beispiel 1: Aktivieren des Schlüsseldepots für das ContosoADLS-Konto</span><span class="sxs-lookup"><span data-stu-id="d3a79-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="d3a79-109">Dieser Befehl versucht, den Benutzer verwalteten schlüsseltresor für das Data Lake Store-Konto mit dem Namen ContosoADLS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d3a79-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="d3a79-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="d3a79-110">PARAMETERS</span></span>

### <span data-ttu-id="d3a79-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="d3a79-111">-Account</span></span>
<span data-ttu-id="d3a79-112">Das Data Lake Store-Konto zum Aktivieren des Benutzer verwalteten Schlüsseldepots für</span><span class="sxs-lookup"><span data-stu-id="d3a79-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

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

### <span data-ttu-id="d3a79-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3a79-113">-DefaultProfile</span></span>
<span data-ttu-id="d3a79-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="d3a79-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d3a79-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3a79-115">-ResourceGroupName</span></span>
<span data-ttu-id="d3a79-116">Der Name der Ressourcengruppe, die dem Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d3a79-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="d3a79-117">Wenn nicht angegeben, wird versucht, erkannt zu werden.</span><span class="sxs-lookup"><span data-stu-id="d3a79-117">If not specified will attempt to be discovered.</span></span>

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

### <span data-ttu-id="d3a79-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="d3a79-118">-Confirm</span></span>
<span data-ttu-id="d3a79-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="d3a79-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3a79-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3a79-120">-WhatIf</span></span>
<span data-ttu-id="d3a79-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="d3a79-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3a79-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d3a79-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3a79-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3a79-123">CommonParameters</span></span>
<span data-ttu-id="d3a79-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d3a79-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3a79-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3a79-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3a79-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="d3a79-126">INPUTS</span></span>

### <span data-ttu-id="d3a79-127">System. String</span><span class="sxs-lookup"><span data-stu-id="d3a79-127">System.String</span></span>

## <span data-ttu-id="d3a79-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="d3a79-128">OUTPUTS</span></span>

### <span data-ttu-id="d3a79-129">System. void</span><span class="sxs-lookup"><span data-stu-id="d3a79-129">System.Void</span></span>

## <span data-ttu-id="d3a79-130">Notizen</span><span class="sxs-lookup"><span data-stu-id="d3a79-130">NOTES</span></span>

## <span data-ttu-id="d3a79-131">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="d3a79-131">RELATED LINKS</span></span>

[<span data-ttu-id="d3a79-132">Neu – AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d3a79-132">New-AzDataLakeStoreAccount</span></span>](./New-AzDataLakeStoreAccount.md)

[<span data-ttu-id="d3a79-133">Satz-AzDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="d3a79-133">Set-AzDataLakeStoreAccount</span></span>](./Set-AzDataLakeStoreAccount.md)

