---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/enable-azurermdatalakestorekeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Enable-AzureRmDataLakeStoreKeyVault.md
ms.openlocfilehash: 062df0ddadc3cc0cfb2e1f0ef9954454b08c4352
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93481257"
---
# <span data-ttu-id="3fd21-101">Enable-AzureRmDataLakeStoreKeyVault</span><span class="sxs-lookup"><span data-stu-id="3fd21-101">Enable-AzureRmDataLakeStoreKeyVault</span></span>

## <span data-ttu-id="3fd21-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="3fd21-102">SYNOPSIS</span></span>
<span data-ttu-id="3fd21-103">Versucht, einen Benutzer verwalteten schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3fd21-103">Attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3fd21-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="3fd21-104">SYNTAX</span></span>

```
Enable-AzureRmDataLakeStoreKeyVault [-Account] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3fd21-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3fd21-105">DESCRIPTION</span></span>
<span data-ttu-id="3fd21-106">Das Cmdlet **enable-AzureRmDataLakeStoreKeyVault** versucht, einen Benutzer verwalteten schlüsseltresor für die Verschlüsselung des angegebenen Data Lake Store-Kontos zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3fd21-106">The **Enable-AzureRmDataLakeStoreKeyVault** cmdlet attempts to enable a user managed Key Vault for encryption of the specified Data Lake Store account.</span></span>

## <span data-ttu-id="3fd21-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="3fd21-107">EXAMPLES</span></span>

### <span data-ttu-id="3fd21-108">Beispiel 1: Aktivieren des Schlüsseldepots für das ContosoADLS-Konto</span><span class="sxs-lookup"><span data-stu-id="3fd21-108">Example 1: Enable the Key Vault for the ContosoADLS account</span></span>
```
PS C:\>Enable-AzureRmDataLakeStoreKeyVault -Name "ContosoADLS"
```

<span data-ttu-id="3fd21-109">Dieser Befehl versucht, den Benutzer verwalteten schlüsseltresor für das Data Lake Store-Konto mit dem Namen ContosoADLS zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3fd21-109">This command attempts to enable the user managed Key Vault for the Data Lake Store account named ContosoADLS.</span></span>

## <span data-ttu-id="3fd21-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="3fd21-110">PARAMETERS</span></span>

### <span data-ttu-id="3fd21-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="3fd21-111">-Account</span></span>
<span data-ttu-id="3fd21-112">Das Data Lake Store-Konto zum Aktivieren des Benutzer verwalteten Schlüsseldepots für</span><span class="sxs-lookup"><span data-stu-id="3fd21-112">The Data Lake Store account to enable the user managed Key Vault for</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName, Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd21-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3fd21-113">-DefaultProfile</span></span>
<span data-ttu-id="3fd21-114">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="3fd21-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3fd21-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3fd21-115">-ResourceGroupName</span></span>
<span data-ttu-id="3fd21-116">Der Name der Ressourcengruppe, die dem Konto zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="3fd21-116">Name of resource group associated with the account.</span></span> <span data-ttu-id="3fd21-117">Wenn nicht angegeben, wird versucht, erkannt zu werden.</span><span class="sxs-lookup"><span data-stu-id="3fd21-117">If not specified will attempt to be discovered.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3fd21-118">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="3fd21-118">-Confirm</span></span>
<span data-ttu-id="3fd21-119">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fd21-119">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd21-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3fd21-120">-WhatIf</span></span>
<span data-ttu-id="3fd21-121">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fd21-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="3fd21-122">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="3fd21-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3fd21-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3fd21-123">CommonParameters</span></span>
<span data-ttu-id="3fd21-124">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3fd21-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3fd21-125">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3fd21-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3fd21-126">Eingaben</span><span class="sxs-lookup"><span data-stu-id="3fd21-126">INPUTS</span></span>

### <span data-ttu-id="3fd21-127">System. String</span><span class="sxs-lookup"><span data-stu-id="3fd21-127">System.String</span></span>

## <span data-ttu-id="3fd21-128">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="3fd21-128">OUTPUTS</span></span>

## <span data-ttu-id="3fd21-129">Notizen</span><span class="sxs-lookup"><span data-stu-id="3fd21-129">NOTES</span></span>

## <span data-ttu-id="3fd21-130">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="3fd21-130">RELATED LINKS</span></span>

[<span data-ttu-id="3fd21-131">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3fd21-131">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="3fd21-132">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="3fd21-132">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

