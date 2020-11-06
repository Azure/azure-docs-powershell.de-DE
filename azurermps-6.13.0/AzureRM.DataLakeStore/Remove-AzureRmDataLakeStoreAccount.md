---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: 585D6C4D-EA80-4E6B-8C36-E7632430431F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreAccount.md
ms.openlocfilehash: 2e73878258a95cf0a7448ba8bfd578e83b69dce6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476113"
---
# <span data-ttu-id="135e5-101">Remove-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="135e5-101">Remove-AzureRmDataLakeStoreAccount</span></span>

## <span data-ttu-id="135e5-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="135e5-102">SYNOPSIS</span></span>
<span data-ttu-id="135e5-103">Löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="135e5-103">Deletes a Data Lake Store account permanently.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="135e5-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="135e5-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreAccount [-Name] <String> [[-ResourceGroupName] <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="135e5-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="135e5-105">DESCRIPTION</span></span>
<span data-ttu-id="135e5-106">Das Cmdlet **Remove-AzureRmDataLakeStoreAccount** löscht ein Data Lake Store-Konto dauerhaft.</span><span class="sxs-lookup"><span data-stu-id="135e5-106">The **Remove-AzureRmDataLakeStoreAccount** cmdlet deletes a Data Lake Store account permanently.</span></span>

## <span data-ttu-id="135e5-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="135e5-107">EXAMPLES</span></span>

### <span data-ttu-id="135e5-108">Beispiel 1: Entfernen eines Data Lake Store-Kontos</span><span class="sxs-lookup"><span data-stu-id="135e5-108">Example 1: Remove a Data Lake Store account</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreAccount -Name "ContosoADL"
```

<span data-ttu-id="135e5-109">Mit diesem Befehl wird das Kontonamens ContosoADL aus dem Data Lake Store entfernt.</span><span class="sxs-lookup"><span data-stu-id="135e5-109">This command removes the account named ContosoADL from the Data Lake Store.</span></span>

## <span data-ttu-id="135e5-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="135e5-110">PARAMETERS</span></span>

### <span data-ttu-id="135e5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="135e5-111">-DefaultProfile</span></span>
<span data-ttu-id="135e5-112">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement</span><span class="sxs-lookup"><span data-stu-id="135e5-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-113">-Force</span><span class="sxs-lookup"><span data-stu-id="135e5-113">-Force</span></span>
<span data-ttu-id="135e5-114">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="135e5-114">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-115">-Name</span><span class="sxs-lookup"><span data-stu-id="135e5-115">-Name</span></span>
<span data-ttu-id="135e5-116">Gibt den Namen des zu entfernenden Kontos an.</span><span class="sxs-lookup"><span data-stu-id="135e5-116">Specifies the name of the account to remove.</span></span>

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

### <span data-ttu-id="135e5-117">-PassThru</span><span class="sxs-lookup"><span data-stu-id="135e5-117">-PassThru</span></span>
<span data-ttu-id="135e5-118">Gibt ein Objekt zurück, das das Element darstellt, mit dem Sie arbeiten.</span><span class="sxs-lookup"><span data-stu-id="135e5-118">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="135e5-119">Standardmäßig wird mit diesem Cmdlet keine Ausgabe generiert.</span><span class="sxs-lookup"><span data-stu-id="135e5-119">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="135e5-120">-ResourceGroupName</span></span>
<span data-ttu-id="135e5-121">Gibt die Ressourcengruppe an, die das zu entfernende Konto enthält.</span><span class="sxs-lookup"><span data-stu-id="135e5-121">Specifies the resource group that contains the account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-122">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="135e5-122">-Confirm</span></span>
<span data-ttu-id="135e5-123">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="135e5-123">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="135e5-124">-WhatIf</span></span>
<span data-ttu-id="135e5-125">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="135e5-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="135e5-126">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="135e5-126">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="135e5-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="135e5-127">CommonParameters</span></span>
<span data-ttu-id="135e5-128">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="135e5-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="135e5-129">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="135e5-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="135e5-130">Eingaben</span><span class="sxs-lookup"><span data-stu-id="135e5-130">INPUTS</span></span>

### <span data-ttu-id="135e5-131">System. String</span><span class="sxs-lookup"><span data-stu-id="135e5-131">System.String</span></span>

## <span data-ttu-id="135e5-132">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="135e5-132">OUTPUTS</span></span>

### <span data-ttu-id="135e5-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="135e5-133">System.Boolean</span></span>

## <span data-ttu-id="135e5-134">Notizen</span><span class="sxs-lookup"><span data-stu-id="135e5-134">NOTES</span></span>

## <span data-ttu-id="135e5-135">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="135e5-135">RELATED LINKS</span></span>

[<span data-ttu-id="135e5-136">Get-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="135e5-136">Get-AzureRmDataLakeStoreAccount</span></span>](./Get-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="135e5-137">Neu – AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="135e5-137">New-AzureRmDataLakeStoreAccount</span></span>](./New-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="135e5-138">Satz-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="135e5-138">Set-AzureRmDataLakeStoreAccount</span></span>](./Set-AzureRmDataLakeStoreAccount.md)

[<span data-ttu-id="135e5-139">Test-AzureRmDataLakeStoreAccount</span><span class="sxs-lookup"><span data-stu-id="135e5-139">Test-AzureRmDataLakeStoreAccount</span></span>](./Test-AzureRmDataLakeStoreAccount.md)


