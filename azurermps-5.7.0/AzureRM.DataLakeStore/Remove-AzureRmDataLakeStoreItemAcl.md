---
external help file: Microsoft.Azure.Commands.DataLakeStore.dll-Help.xml
Module Name: AzureRM.DataLakeStore
ms.assetid: D3E8A6A6-C6C5-46B0-914B-75088A6F6011
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakestore/remove-azurermdatalakestoreitemacl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeStore/Commands.DataLakeStore/help/Remove-AzureRmDataLakeStoreItemAcl.md
ms.openlocfilehash: 23eb57a6c12c3ce5ba8334b7309b5c282624620a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/20/2020
ms.locfileid: "93476790"
---
# <span data-ttu-id="31d88-101">Remove-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="31d88-101">Remove-AzureRmDataLakeStoreItemAcl</span></span>

## <span data-ttu-id="31d88-102">Synopsis</span><span class="sxs-lookup"><span data-stu-id="31d88-102">SYNOPSIS</span></span>
<span data-ttu-id="31d88-103">Löscht die ACL einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31d88-103">Clears the ACL of a file or folder in Data Lake Store.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31d88-104">Syntax</span><span class="sxs-lookup"><span data-stu-id="31d88-104">SYNTAX</span></span>

```
Remove-AzureRmDataLakeStoreItemAcl [-Account] <String> [-Path] <DataLakeStorePathInstance> [-Default] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="31d88-105">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31d88-105">DESCRIPTION</span></span>
<span data-ttu-id="31d88-106">Das Cmdlet **Remove-AzureRmDataLakeStoreItemAcl** löscht die Zugriffssteuerungsliste (ACL) einer Datei oder eines Ordners im Data Lake Store.</span><span class="sxs-lookup"><span data-stu-id="31d88-106">The **Remove-AzureRmDataLakeStoreItemAcl** cmdlet clears the access control list (ACL) of a file or folder in Data Lake Store.</span></span>

## <span data-ttu-id="31d88-107">Beispiele</span><span class="sxs-lookup"><span data-stu-id="31d88-107">EXAMPLES</span></span>

### <span data-ttu-id="31d88-108">Beispiel 1: Entfernen der ACL aus einem Ordner</span><span class="sxs-lookup"><span data-stu-id="31d88-108">Example 1: Remove the ACL from a folder</span></span>
```
PS C:\>Remove-AzureRmDataLakeStoreItemAcl -AccountName "ContosoADL" -Path "/"
```

<span data-ttu-id="31d88-109">Dieser Befehl entfernt die ACL für das Stammverzeichnis für das ContosoADL-Konto.</span><span class="sxs-lookup"><span data-stu-id="31d88-109">This command removes the ACL for the root directory for the ContosoADL account.</span></span>

## <span data-ttu-id="31d88-110">Parameter</span><span class="sxs-lookup"><span data-stu-id="31d88-110">PARAMETERS</span></span>

### <span data-ttu-id="31d88-111">-Konto</span><span class="sxs-lookup"><span data-stu-id="31d88-111">-Account</span></span>
<span data-ttu-id="31d88-112">Gibt den Namen des Daten Lake Store-Kontos an.</span><span class="sxs-lookup"><span data-stu-id="31d88-112">Specifies the Data Lake Store account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-113">– Standard</span><span class="sxs-lookup"><span data-stu-id="31d88-113">-Default</span></span>
<span data-ttu-id="31d88-114">Gibt an, dass das Cmdlet die Standard-ACL für eine Datei oder einen Ordner entfernt.</span><span class="sxs-lookup"><span data-stu-id="31d88-114">Indicates that the cmdlet removes the default ACL for a file or a folder.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31d88-115">-DefaultProfile</span></span>
<span data-ttu-id="31d88-116">Die für die Kommunikation mit Azure verwendeten Anmeldeinformationen, das Konto, den Mandanten und das Abonnement.</span><span class="sxs-lookup"><span data-stu-id="31d88-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31d88-117">-Force</span><span class="sxs-lookup"><span data-stu-id="31d88-117">-Force</span></span>
<span data-ttu-id="31d88-118">Erzwingt, dass der Befehl ausgeführt wird, ohne die Bestätigung des Benutzers zu fordern.</span><span class="sxs-lookup"><span data-stu-id="31d88-118">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="31d88-119">-PassThru</span></span>
<span data-ttu-id="31d88-120">Gibt an, dass eine boolesche Antwort zurückgegeben werden soll, die das Ergebnis des Löschvorgangs angibt.</span><span class="sxs-lookup"><span data-stu-id="31d88-120">Indicates a boolean response should be returned indicating the result of the delete operation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-121">-Path</span><span class="sxs-lookup"><span data-stu-id="31d88-121">-Path</span></span>
<span data-ttu-id="31d88-122">Gibt den Daten See-Speicherpfad des Elements an, beginnend mit dem Stammverzeichnis (/).</span><span class="sxs-lookup"><span data-stu-id="31d88-122">Specifies the Data Lake Store path of the item, starting with the root directory (/).</span></span>

```yaml
Type: DataLakeStorePathInstance
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-123">-Bestätigen</span><span class="sxs-lookup"><span data-stu-id="31d88-123">-Confirm</span></span>
<span data-ttu-id="31d88-124">Sie werden zur Bestätigung aufgefordert, bevor Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="31d88-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="31d88-125">-WhatIf</span></span>
<span data-ttu-id="31d88-126">Zeigt, was passiert, wenn das Cmdlet ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="31d88-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="31d88-127">Das Cmdlet wird nicht ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="31d88-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="31d88-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31d88-128">CommonParameters</span></span>
<span data-ttu-id="31d88-129">Dieses Cmdlet unterstützt die allgemeinen Parameter:-Debug,-Fehler Aktion,-ErrorVariable,-InformationVariable,-Variable,-Puffer,-PipelineVariable,-Verbose,-Warning-Aktion und-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="31d88-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31d88-130">Weitere Informationen finden Sie unter about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31d88-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31d88-131">Eingaben</span><span class="sxs-lookup"><span data-stu-id="31d88-131">INPUTS</span></span>

### <span data-ttu-id="31d88-132">Keine</span><span class="sxs-lookup"><span data-stu-id="31d88-132">None</span></span>
<span data-ttu-id="31d88-133">Dieses Cmdlet akzeptiert keine Eingaben.</span><span class="sxs-lookup"><span data-stu-id="31d88-133">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="31d88-134">Ausgaben</span><span class="sxs-lookup"><span data-stu-id="31d88-134">OUTPUTS</span></span>

### <span data-ttu-id="31d88-135">bool</span><span class="sxs-lookup"><span data-stu-id="31d88-135">bool</span></span>
<span data-ttu-id="31d88-136">Wenn passthru angegeben ist, wird nach dem erfolgreichen Abschluss "true" zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="31d88-136">If PassThru is specified, returns true upon successful completion.</span></span>

## <span data-ttu-id="31d88-137">Notizen</span><span class="sxs-lookup"><span data-stu-id="31d88-137">NOTES</span></span>
* <span data-ttu-id="31d88-138">Alias: Remove-AdlStoreAcl</span><span class="sxs-lookup"><span data-stu-id="31d88-138">Alias: Remove-AdlStoreAcl</span></span>

## <span data-ttu-id="31d88-139">Verwandte Links</span><span class="sxs-lookup"><span data-stu-id="31d88-139">RELATED LINKS</span></span>

[<span data-ttu-id="31d88-140">Get-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31d88-140">Get-AzureRmDataLakeStoreItemAclEntry</span></span>](./Get-AzureRmDataLakeStoreItemAclEntry.md)

[<span data-ttu-id="31d88-141">Satz-AzureRmDataLakeStoreItemAcl</span><span class="sxs-lookup"><span data-stu-id="31d88-141">Set-AzureRmDataLakeStoreItemAcl</span></span>](./Set-AzureRmDataLakeStoreItemAcl.md)

[<span data-ttu-id="31d88-142">Satz-AzureRmDataLakeStoreItemAclEntry</span><span class="sxs-lookup"><span data-stu-id="31d88-142">Set-AzureRmDataLakeStoreItemAclEntry</span></span>](./Set-AzureRmDataLakeStoreItemAclEntry.md)


