---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: AFDE5ECD-29AB-4C91-98BF-1B8C9C3BB079
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchaccountkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchAccountKey.md
ms.openlocfilehash: 2662eeeeaedbac75f443bf6160c625dfdb8dd854
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/27/2020
ms.locfileid: "94303778"
---
# <span data-ttu-id="23d10-101">Get-AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="23d10-101">Get-AzBatchAccountKey</span></span>

## <span data-ttu-id="23d10-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="23d10-102">SYNOPSIS</span></span>
<span data-ttu-id="23d10-103">Ruft die Schlüssel eines Batch Kontos ab.</span><span class="sxs-lookup"><span data-stu-id="23d10-103">Gets the keys of a Batch account.</span></span>

## <span data-ttu-id="23d10-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="23d10-104">SYNTAX</span></span>

```
Get-AzBatchAccountKey [-AccountName] <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="23d10-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="23d10-105">DESCRIPTION</span></span>
<span data-ttu-id="23d10-106">Das Cmdlet " **Get-AzBatchAccountKey** " Ruft die Schlüssel eines Azure-Batch Kontos im aktuellen Abonnement ab.</span><span class="sxs-lookup"><span data-stu-id="23d10-106">The **Get-AzBatchAccountKey** cmdlet gets the keys of an Azure Batch account in the current subscription.</span></span>

## <span data-ttu-id="23d10-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="23d10-107">EXAMPLES</span></span>

### <span data-ttu-id="23d10-108">Beispiel 1: Abrufen von Batch Konto Schlüsseln und speichern in $context Variable zur späteren Verwendung</span><span class="sxs-lookup"><span data-stu-id="23d10-108">Example 1: Get batch account keys and save it in $Context variable for use later</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
```

<span data-ttu-id="23d10-109">Dieser Befehl ruft die Kontodetails ab und speichert Sie in einem `$Context` Objekt, um Sie später verwenden zu können.</span><span class="sxs-lookup"><span data-stu-id="23d10-109">This command gets the account details and stores it in a `$Context` object for use later.</span></span>

### <span data-ttu-id="23d10-110">Beispiel 2: Abrufen von Stapel Konto Schlüsseln und Anzeigen der Schlüssel</span><span class="sxs-lookup"><span data-stu-id="23d10-110">Example 2: Get batch account keys and display them</span></span>
```
PS C:\>$Context = Get-AzBatchAccountKey -AccountName myaccount
PS C:\>$Context.PrimaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
PS C:\>$Context.SecondaryAccountKey
ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMNOPQRSTUVWXYZ0123456789ABCDEFGHIJKLMN==
```

<span data-ttu-id="23d10-111">Mit diesem Befehl werden die Kontoschlüssel abgerufen und auf der Konsole gedruckt.</span><span class="sxs-lookup"><span data-stu-id="23d10-111">This command gets the account keys and prints them to the console.</span></span>

## <span data-ttu-id="23d10-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="23d10-112">PARAMETERS</span></span>

### <span data-ttu-id="23d10-113">-Kontoname</span><span class="sxs-lookup"><span data-stu-id="23d10-113">-AccountName</span></span>
<span data-ttu-id="23d10-114">Gibt den Namen des Kontos an, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="23d10-114">Specifies the name of the account for which this cmdlet gets keys.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="23d10-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23d10-115">-DefaultProfile</span></span>
<span data-ttu-id="23d10-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="23d10-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23d10-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23d10-117">-ResourceGroupName</span></span>
<span data-ttu-id="23d10-118">Gibt den Namen der Ressourcengruppe an, die das Konto enthält, für das dieses Cmdlet Schlüssel erhält.</span><span class="sxs-lookup"><span data-stu-id="23d10-118">Specifies the name of the resource group that contains the account for which this cmdlet gets keys.</span></span>

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

### <span data-ttu-id="23d10-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23d10-119">CommonParameters</span></span>
<span data-ttu-id="23d10-120">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="23d10-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23d10-121">Weitere Informationen finden Sie unter [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="23d10-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23d10-122">Eingaben</span><span class="sxs-lookup"><span data-stu-id="23d10-122">INPUTS</span></span>

### <span data-ttu-id="23d10-123">System. String</span><span class="sxs-lookup"><span data-stu-id="23d10-123">System.String</span></span>

## <span data-ttu-id="23d10-124">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="23d10-124">OUTPUTS</span></span>

### <span data-ttu-id="23d10-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span><span class="sxs-lookup"><span data-stu-id="23d10-125">Microsoft.Azure.Commands.Batch.BatchAccountContext</span></span>

## <span data-ttu-id="23d10-126">Notizen</span><span class="sxs-lookup"><span data-stu-id="23d10-126">NOTES</span></span>

## <span data-ttu-id="23d10-127">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="23d10-127">RELATED LINKS</span></span>

[<span data-ttu-id="23d10-128">Neu – AzBatchAccountKey</span><span class="sxs-lookup"><span data-stu-id="23d10-128">New-AzBatchAccountKey</span></span>](./New-AzBatchAccountKey.md)

[<span data-ttu-id="23d10-129">Azure Batch-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="23d10-129">Azure Batch Cmdlets</span></span>](/powershell/module/Az.Batch/)
